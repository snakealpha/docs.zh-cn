---
title: "ICLRTaskManager::SetUILocale 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRTaskManager.SetUILocale
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRTaskManager::SetUILocale
helpviewer_keywords:
- ICLRTaskManager::SetUILocale method [.NET Framework hosting]
- SetUILocale method, ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 03adaa9a-2beb-49b3-b2c4-6b4fc3f10715
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 28ecba8b88ceadaf743f5c65bc6f257f7ef8cd60
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="iclrtaskmanagersetuilocale-method"></a><span data-ttu-id="3d90a-102">ICLRTaskManager::SetUILocale 方法</span><span class="sxs-lookup"><span data-stu-id="3d90a-102">ICLRTaskManager::SetUILocale Method</span></span>
<span data-ttu-id="3d90a-103">将公共语言运行时 (CLR) 主机已修改的用户界面 (UI) 区域设置或区域性，通知当前正在执行的任务。</span><span class="sxs-lookup"><span data-stu-id="3d90a-103">Notifies the common language runtime (CLR) that the host has modified the user interface (UI) locale, or culture, on the currently executing task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d90a-104">语法</span><span class="sxs-lookup"><span data-stu-id="3d90a-104">Syntax</span></span>  
  
```  
HRESULT SetUILocale (  
    [in] LCID lcid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3d90a-105">参数</span><span class="sxs-lookup"><span data-stu-id="3d90a-105">Parameters</span></span>  
 `lcid`  
 <span data-ttu-id="3d90a-106">[in]映射到新分配的地理区域性和用户界面的语言区域设置标识符值。</span><span class="sxs-lookup"><span data-stu-id="3d90a-106">[in] The locale identifier value that maps to the newly assigned geographical culture and language for the user interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3d90a-107">返回值</span><span class="sxs-lookup"><span data-stu-id="3d90a-107">Return Value</span></span>  
  
|<span data-ttu-id="3d90a-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3d90a-108">HRESULT</span></span>|<span data-ttu-id="3d90a-109">描述</span><span class="sxs-lookup"><span data-stu-id="3d90a-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3d90a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d90a-110">S_OK</span></span>|<span data-ttu-id="3d90a-111">`SetUILocale`已成功返回。</span><span class="sxs-lookup"><span data-stu-id="3d90a-111">`SetUILocale` returned successfully.</span></span>|  
|<span data-ttu-id="3d90a-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3d90a-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3d90a-113">CLR 尚未加载到进程中，或 CLR 处于不能运行托管的代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="3d90a-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3d90a-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3d90a-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3d90a-115">调用操作已超时。</span><span class="sxs-lookup"><span data-stu-id="3d90a-115">The call timed out.</span></span>|  
|<span data-ttu-id="3d90a-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3d90a-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3d90a-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="3d90a-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3d90a-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3d90a-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3d90a-119">事件已被取消时被阻塞的线程，或者纤程正在等待它。</span><span class="sxs-lookup"><span data-stu-id="3d90a-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3d90a-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3d90a-120">E_FAIL</span></span>|<span data-ttu-id="3d90a-121">出现未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="3d90a-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3d90a-122">如果某方法返回 E_FAIL，CLR 不再可用进程内。</span><span class="sxs-lookup"><span data-stu-id="3d90a-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3d90a-123">到托管方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="3d90a-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3d90a-124">备注</span><span class="sxs-lookup"><span data-stu-id="3d90a-124">Remarks</span></span>  
 <span data-ttu-id="3d90a-125">`SetUILocale`提供要执行的区域设置的同步可能会显示任何机制的主机的机会。</span><span class="sxs-lookup"><span data-stu-id="3d90a-125">`SetUILocale` provides an opportunity for the host to execute any mechanisms it might have for the synchronization of locales.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d90a-126">要求</span><span class="sxs-lookup"><span data-stu-id="3d90a-126">Requirements</span></span>  
 <span data-ttu-id="3d90a-127">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3d90a-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d90a-128">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3d90a-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3d90a-129">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="3d90a-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3d90a-130">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d90a-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d90a-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d90a-131">See Also</span></span>  
 [<span data-ttu-id="3d90a-132">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="3d90a-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="3d90a-133">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3d90a-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="3d90a-134">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="3d90a-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="3d90a-135">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="3d90a-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)