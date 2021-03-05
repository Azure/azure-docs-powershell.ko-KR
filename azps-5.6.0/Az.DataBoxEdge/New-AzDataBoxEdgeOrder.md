---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 668b7be0a4c6f9885bf8ebb3a077d58f99b681fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978640"
---
# <span data-ttu-id="55e85-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="55e85-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="55e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e85-102">SYNOPSIS</span></span>
<span data-ttu-id="55e85-103">디바이스에 대한 새 주문을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="55e85-104">구문</span><span class="sxs-lookup"><span data-stu-id="55e85-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e85-105">설명</span><span class="sxs-lookup"><span data-stu-id="55e85-105">DESCRIPTION</span></span>
<span data-ttu-id="55e85-106">**New-AzDataBoxEdgeOrder** cmdlet은 Data Box Edge 디바이스에 대한 새 순서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="55e85-107">Data Box Edge 디바이스 리소스는 주문을 만들기 전에 먼저 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="55e85-108">연락처, 회사 이름, 전자 메일, 주소 등의 세부 정보를 주문을 만드는 매개 변수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="55e85-109">예제</span><span class="sxs-lookup"><span data-stu-id="55e85-109">EXAMPLES</span></span>

### <span data-ttu-id="55e85-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="55e85-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="55e85-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55e85-111">PARAMETERS</span></span>

### <span data-ttu-id="55e85-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="55e85-112">-AddressLine1</span></span>
<span data-ttu-id="55e85-113">첫 번째 줄 주소</span><span class="sxs-lookup"><span data-stu-id="55e85-113">Address first line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="55e85-114">-AddressLine2</span></span>
<span data-ttu-id="55e85-115">주소 두 번째 줄</span><span class="sxs-lookup"><span data-stu-id="55e85-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="55e85-116">-AddressLine3</span></span>
<span data-ttu-id="55e85-117">주소 세 번째 줄</span><span class="sxs-lookup"><span data-stu-id="55e85-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55e85-118">-AsJob</span></span>
<span data-ttu-id="55e85-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="55e85-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-120">-City</span><span class="sxs-lookup"><span data-stu-id="55e85-120">-City</span></span>
<span data-ttu-id="55e85-121">도시의 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-121">Name of the City</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="55e85-122">-CompanyName</span></span>
<span data-ttu-id="55e85-123">회사의 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-123">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="55e85-124">-ContactPerson</span></span>
<span data-ttu-id="55e85-125">연락처 사람의 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-125">Name of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-126">-Country</span><span class="sxs-lookup"><span data-stu-id="55e85-126">-Country</span></span>
<span data-ttu-id="55e85-127">국가 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-127">Name of the Country</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e85-128">-DefaultProfile</span></span>
<span data-ttu-id="55e85-129">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="55e85-130">-DeviceName</span></span>
<span data-ttu-id="55e85-131">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-132">-email</span><span class="sxs-lookup"><span data-stu-id="55e85-132">-Email</span></span>
<span data-ttu-id="55e85-133">업데이트를 받을 전자 메일 목록, 최대 10개 전자 메일 수락</span><span class="sxs-lookup"><span data-stu-id="55e85-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="55e85-134">-Phone</span></span>
<span data-ttu-id="55e85-135">연락처 사람의 전화 번호</span><span class="sxs-lookup"><span data-stu-id="55e85-135">Phone number of the contact person</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="55e85-136">-PostalCode</span></span>
<span data-ttu-id="55e85-137">주소의 우편 번호</span><span class="sxs-lookup"><span data-stu-id="55e85-137">Postal Code of the Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e85-138">-ResourceGroupName</span></span>
<span data-ttu-id="55e85-139">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-140">-State</span><span class="sxs-lookup"><span data-stu-id="55e85-140">-State</span></span>
<span data-ttu-id="55e85-141">상태 이름</span><span class="sxs-lookup"><span data-stu-id="55e85-141">Name of the State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-142">-확인</span><span class="sxs-lookup"><span data-stu-id="55e85-142">-Confirm</span></span>
<span data-ttu-id="55e85-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e85-144">-WhatIf</span></span>
<span data-ttu-id="55e85-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55e85-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e85-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e85-147">CommonParameters</span></span>
<span data-ttu-id="55e85-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55e85-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e85-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55e85-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e85-150">입력</span><span class="sxs-lookup"><span data-stu-id="55e85-150">INPUTS</span></span>

### <span data-ttu-id="55e85-151">System.String</span><span class="sxs-lookup"><span data-stu-id="55e85-151">System.String</span></span>

## <span data-ttu-id="55e85-152">출력</span><span class="sxs-lookup"><span data-stu-id="55e85-152">OUTPUTS</span></span>

### <span data-ttu-id="55e85-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="55e85-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="55e85-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55e85-154">NOTES</span></span>

## <span data-ttu-id="55e85-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55e85-155">RELATED LINKS</span></span>
