---
title: "记录 (F#)"
description: "了解如何对 F # 记录表示已命名的值，并且可选择带有成员的简单聚合。"
keywords: "visual f#, f#, 函数编程"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 3a3701ea-4308-4fa1-9b5c-b955c470f17a
ms.openlocfilehash: f5ade1db39431d99f10eb6967f02335123b83d34
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="records"></a><span data-ttu-id="7ce76-104">记录</span><span class="sxs-lookup"><span data-stu-id="7ce76-104">Records</span></span>

<span data-ttu-id="7ce76-105">记录表示已命名值的简单聚合，可选择包含成员。</span><span class="sxs-lookup"><span data-stu-id="7ce76-105">Records represent simple aggregates of named values, optionally with members.</span></span>  <span data-ttu-id="7ce76-106">F # 4.1 开始，它们可以是结构或引用类型。</span><span class="sxs-lookup"><span data-stu-id="7ce76-106">Starting with F# 4.1, they can either be structs or reference types.</span></span>  <span data-ttu-id="7ce76-107">它们是引用类型，默认情况下。</span><span class="sxs-lookup"><span data-stu-id="7ce76-107">They are reference types by default.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce76-108">语法</span><span class="sxs-lookup"><span data-stu-id="7ce76-108">Syntax</span></span>

```fsharp
[ attributes ]
type [accessibility-modifier] typename = {
    [ mutable ] label1 : type1;
    [ mutable ] label2 : type2;
    ...
}
    [ member-list ]
```

## <a name="remarks"></a><span data-ttu-id="7ce76-109">备注</span><span class="sxs-lookup"><span data-stu-id="7ce76-109">Remarks</span></span>
<span data-ttu-id="7ce76-110">在上述语法中， *typename*是记录类型的名称*label1*和*label2*是名称的值，称为*标签*，和*type1*和*type2*是这些值的类型。</span><span class="sxs-lookup"><span data-stu-id="7ce76-110">In the previous syntax, *typename* is the name of the record type, *label1* and *label2* are names of values, referred to as *labels*, and *type1* and *type2* are the types of these values.</span></span> <span data-ttu-id="7ce76-111">*成员列表中*是类型的成员的可选列表。</span><span class="sxs-lookup"><span data-stu-id="7ce76-111">*member-list* is the optional list of members for the type.</span></span>  <span data-ttu-id="7ce76-112">你可以使用`[<Struct>]`属性来创建结构记录而不是这是引用类型的记录。</span><span class="sxs-lookup"><span data-stu-id="7ce76-112">You can use the `[<Struct>]` attribute to create a struct record rather than a record which is a reference type.</span></span>

<span data-ttu-id="7ce76-113">以下是一些示例。</span><span class="sxs-lookup"><span data-stu-id="7ce76-113">Following are some examples.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1901.fs)]

<span data-ttu-id="7ce76-114">在单独一行上每个标签时，分号是可选的。</span><span class="sxs-lookup"><span data-stu-id="7ce76-114">When each label is on a separate line, the semicolon is optional.</span></span>

<span data-ttu-id="7ce76-115">你可以在称为表达式中设置值*记录表达式*。</span><span class="sxs-lookup"><span data-stu-id="7ce76-115">You can set values in expressions known as *record expressions*.</span></span> <span data-ttu-id="7ce76-116">编译器推断出的类型中使用 （如果标签都足够不同于其他记录类型） 的标签。</span><span class="sxs-lookup"><span data-stu-id="7ce76-116">The compiler infers the type from the labels used (if the labels are sufficiently distinct from those of other record types).</span></span> <span data-ttu-id="7ce76-117">大括号 （{}） 括住记录表达式。</span><span class="sxs-lookup"><span data-stu-id="7ce76-117">Braces ({ }) enclose the record expression.</span></span> <span data-ttu-id="7ce76-118">下面的代码演示初始化带有标签的三个浮点元素的记录的记录表达式`x`，`y`和`z`。</span><span class="sxs-lookup"><span data-stu-id="7ce76-118">The following code shows a record expression that initializes a record with three float elements with labels `x`, `y` and `z`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1907.fs)]

<span data-ttu-id="7ce76-119">如果可以还具有相同的标签的另一种类型，则不使用缩写形式。</span><span class="sxs-lookup"><span data-stu-id="7ce76-119">Do not use the shortened form if there could be another type that also has the same labels.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1903.fs)]

<span data-ttu-id="7ce76-120">最近声明的类型的标签优先于那些以前声明的类型，因此，在前面的示例中，`mypoint3D`将被推断`Point3D`。</span><span class="sxs-lookup"><span data-stu-id="7ce76-120">The labels of the most recently declared type take precedence over those of the previously declared type, so in the preceding example, `mypoint3D` is inferred to be `Point3D`.</span></span> <span data-ttu-id="7ce76-121">你可以显式指定记录类型，如以下代码所示。</span><span class="sxs-lookup"><span data-stu-id="7ce76-121">You can explicitly specify the record type, as in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1908.fs)]

<span data-ttu-id="7ce76-122">可以定义与类类型的记录类型的方法。</span><span class="sxs-lookup"><span data-stu-id="7ce76-122">Methods can be defined for record types just as for class types.</span></span>

## <a name="creating-records-by-using-record-expressions"></a><span data-ttu-id="7ce76-123">通过使用记录表达式创建记录</span><span class="sxs-lookup"><span data-stu-id="7ce76-123">Creating Records by Using Record Expressions</span></span>
<span data-ttu-id="7ce76-124">可以通过使用记录中定义的标签来初始化记录。</span><span class="sxs-lookup"><span data-stu-id="7ce76-124">You can initialize records by using the labels that are defined in the record.</span></span> <span data-ttu-id="7ce76-125">表达式可完成此称为*记录表达式*。</span><span class="sxs-lookup"><span data-stu-id="7ce76-125">An expression that does this is referred to as a *record expression*.</span></span> <span data-ttu-id="7ce76-126">使用括号来括住记录表达式，并使用分号作为分隔符。</span><span class="sxs-lookup"><span data-stu-id="7ce76-126">Use braces to enclose the record expression and use the semicolon as a delimiter.</span></span>

<span data-ttu-id="7ce76-127">下面的示例演示如何创建一条记录。</span><span class="sxs-lookup"><span data-stu-id="7ce76-127">The following example shows how to create a record.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1904.fs)]

<span data-ttu-id="7ce76-128">最后一个字段中记录表达式和类型定义中后面的分号是可选的而不考虑字段是否都在同一行。</span><span class="sxs-lookup"><span data-stu-id="7ce76-128">The semicolons after the last field in the record expression and in the type definition are optional, regardless of whether the fields are all in one line.</span></span>

<span data-ttu-id="7ce76-129">创建一条记录时，您必须提供每个字段的值。</span><span class="sxs-lookup"><span data-stu-id="7ce76-129">When you create a record, you must supply values for each field.</span></span> <span data-ttu-id="7ce76-130">你不能引用的任何字段的初始化表达式中的其他字段的值。</span><span class="sxs-lookup"><span data-stu-id="7ce76-130">You cannot refer to the values of other fields in the initialization expression for any field.</span></span>

<span data-ttu-id="7ce76-131">在下面的代码的一种`myRecord2`推断出的字段的名称。</span><span class="sxs-lookup"><span data-stu-id="7ce76-131">In the following code, the type of `myRecord2` is inferred from the names of the fields.</span></span> <span data-ttu-id="7ce76-132">（可选） 你可以显式指定类型名称。</span><span class="sxs-lookup"><span data-stu-id="7ce76-132">Optionally, you can specify the type name explicitly.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1905.fs)]

<span data-ttu-id="7ce76-133">如果你需要复制现有记录，并可能会更改某些字段值，可记录构造的另一种形式。</span><span class="sxs-lookup"><span data-stu-id="7ce76-133">Another form of record construction can be useful when you have to copy an existing record, and possibly change some of the field values.</span></span> <span data-ttu-id="7ce76-134">以下代码行阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="7ce76-134">The following line of code illustrates this.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1906.fs)]

<span data-ttu-id="7ce76-135">这种形式的记录表达式称为*复制和更新记录表达式*。</span><span class="sxs-lookup"><span data-stu-id="7ce76-135">This form of the record expression is called the *copy and update record expression*.</span></span>

<span data-ttu-id="7ce76-136">记录是不可变的默认设置。但是，你可以使用复制和更新表达式来轻松创建已修改的记录。</span><span class="sxs-lookup"><span data-stu-id="7ce76-136">Records are immutable by default; however, you can easily create modified records by using a copy and update expression.</span></span> <span data-ttu-id="7ce76-137">你还可显式指定可变字段。</span><span class="sxs-lookup"><span data-stu-id="7ce76-137">You can also explicitly specify a mutable field.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1909.fs)]

<span data-ttu-id="7ce76-138">不要将用于记录字段的 DefaultValue 特性。</span><span class="sxs-lookup"><span data-stu-id="7ce76-138">Don't use the DefaultValue attribute with record fields.</span></span> <span data-ttu-id="7ce76-139">更好的方法是定义具有初始化的字段的记录的默认实例为默认值，使用的副本，然后更新记录表达式来设置所有与默认值不同的字段。</span><span class="sxs-lookup"><span data-stu-id="7ce76-139">A better approach is to define default instances of records with fields that are initialized to default values and then use a copy and update record expression to set any fields that differ from the default values.</span></span>

```fsharp
// Rather than use [<DefaultValue>], define a default record.
type MyRecord =
{
    field1 : int
    field2 : int
}

let defaultRecord1 = { field1 = 0; field2 = 0 }
let defaultRecord2 = { field1 = 1; field2 = 25 }

// Use the with keyword to populate only a few chosen fields
// and leave the rest with default values.
let rr3 = { defaultRecord1 with field2 = 42 }
```

## <a name="pattern-matching-with-records"></a><span data-ttu-id="7ce76-140">使用记录的模式匹配</span><span class="sxs-lookup"><span data-stu-id="7ce76-140">Pattern Matching with Records</span></span>
<span data-ttu-id="7ce76-141">记录可以与模式匹配一起使用。</span><span class="sxs-lookup"><span data-stu-id="7ce76-141">Records can be used with pattern matching.</span></span> <span data-ttu-id="7ce76-142">可以显式指定一些字段，并为变量的匹配项时将分配其他字段中提供。</span><span class="sxs-lookup"><span data-stu-id="7ce76-142">You can specify some fields explicitly and provide variables for other fields that will be assigned when a match occurs.</span></span> <span data-ttu-id="7ce76-143">下面的代码示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="7ce76-143">The following code example illustrates this.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1910.fs)]

<span data-ttu-id="7ce76-144">此代码的输出如下所示。</span><span class="sxs-lookup"><span data-stu-id="7ce76-144">The output of this code is as follows.</span></span>

```
Point is at the origin.
Point is on the x-axis. Value is 100.000000.
Point is at (10.000000, 0.000000, -1.000000).
```

## <a name="differences-between-records-and-classes"></a><span data-ttu-id="7ce76-145">记录和类之间的差异</span><span class="sxs-lookup"><span data-stu-id="7ce76-145">Differences Between Records and Classes</span></span>
<span data-ttu-id="7ce76-146">因为它们会自动公开为属性，并且它们是用于创建和复制的记录，记录的字段与类不同。</span><span class="sxs-lookup"><span data-stu-id="7ce76-146">Record fields differ from classes in that they are automatically exposed as properties, and they are used in the creation and copying of records.</span></span> <span data-ttu-id="7ce76-147">记录构造也不同于类构造。</span><span class="sxs-lookup"><span data-stu-id="7ce76-147">Record construction also differs from class construction.</span></span> <span data-ttu-id="7ce76-148">在记录类型，不能定义构造函数。</span><span class="sxs-lookup"><span data-stu-id="7ce76-148">In a record type, you cannot define a constructor.</span></span> <span data-ttu-id="7ce76-149">相反，本主题中所述的构造语法适用。</span><span class="sxs-lookup"><span data-stu-id="7ce76-149">Instead, the construction syntax described in this topic applies.</span></span> <span data-ttu-id="7ce76-150">类具有构造函数参数、 字段和属性之间没有直接关系。</span><span class="sxs-lookup"><span data-stu-id="7ce76-150">Classes have no direct relationship between constructor parameters, fields, and properties.</span></span>

<span data-ttu-id="7ce76-151">与联合和结构类型，类似记录具有结构上相等语义。</span><span class="sxs-lookup"><span data-stu-id="7ce76-151">Like union and structure types, records have structural equality semantics.</span></span> <span data-ttu-id="7ce76-152">类具有引用相等性语义。</span><span class="sxs-lookup"><span data-stu-id="7ce76-152">Classes have reference equality semantics.</span></span> <span data-ttu-id="7ce76-153">下面的代码示例说明这一点。</span><span class="sxs-lookup"><span data-stu-id="7ce76-153">The following code example demonstrates this.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1911.fs)]

<span data-ttu-id="7ce76-154">如果您编写与类相同的代码，两个类对象则不相等，因为两个值表示堆上的两个对象，并仅地址进行比较 (除非类类型替代`System.Object.Equals`方法)。</span><span class="sxs-lookup"><span data-stu-id="7ce76-154">If you write the same code with classes, the two class objects would be unequal because the two values would represent two objects on the heap and only the addresses would be compared (unless the class type overrides the `System.Object.Equals` method).</span></span>

<span data-ttu-id="7ce76-155">如果你需要引用记录是否相等，则将属性添加`[<ReferenceEquality>]`记录上方。</span><span class="sxs-lookup"><span data-stu-id="7ce76-155">If you need reference equality for records, add the attribute `[<ReferenceEquality>]` above the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ce76-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ce76-156">See Also</span></span>
[<span data-ttu-id="7ce76-157">F# 类型</span><span class="sxs-lookup"><span data-stu-id="7ce76-157">F# Types</span></span>](fsharp-types.md)

[<span data-ttu-id="7ce76-158">类</span><span class="sxs-lookup"><span data-stu-id="7ce76-158">Classes</span></span>](classes.md)

[<span data-ttu-id="7ce76-159">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="7ce76-159">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="7ce76-160">引用相等性</span><span class="sxs-lookup"><span data-stu-id="7ce76-160">Reference-Equality</span></span>](https://msdn.microsoft.com/en-us/visualfsharpdocs/conceptual/core.referenceequalityattribute-class-%5bfsharp%5d)

[<span data-ttu-id="7ce76-161">模式匹配</span><span class="sxs-lookup"><span data-stu-id="7ce76-161">Pattern Matching</span></span>](pattern-matching.md)