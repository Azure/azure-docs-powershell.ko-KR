---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209136"
---
# <span data-ttu-id="3e0fe-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="3e0fe-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="3e0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0fe-103">디바이스에 대한 새 주문을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="3e0fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e0fe-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e0fe-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e0fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3e0fe-106">**New-AzStackEdgeOrder** cmdlet은 Stack Edge 디바이스에 대한 새 순서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="3e0fe-107">주문을 만들기 전에 Stack Edge 디바이스 리소스를 먼저 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="3e0fe-108">연락처 사람, 회사 이름, 전자 메일, 주소 등의 세부 정보를 주문을 만들기 위한 매개 변수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="3e0fe-109">예제</span><span class="sxs-lookup"><span data-stu-id="3e0fe-109">EXAMPLES</span></span>

### <span data-ttu-id="3e0fe-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e0fe-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="3e0fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e0fe-111">PARAMETERS</span></span>

### <span data-ttu-id="3e0fe-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="3e0fe-112">-AddressLine1</span></span>
<span data-ttu-id="3e0fe-113">첫 줄 주소</span><span class="sxs-lookup"><span data-stu-id="3e0fe-113">Address first line</span></span>

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

### <span data-ttu-id="3e0fe-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="3e0fe-114">-AddressLine2</span></span>
<span data-ttu-id="3e0fe-115">주소 두 번째 줄</span><span class="sxs-lookup"><span data-stu-id="3e0fe-115">Address second line</span></span>

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

### <span data-ttu-id="3e0fe-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="3e0fe-116">-AddressLine3</span></span>
<span data-ttu-id="3e0fe-117">세 번째 줄 주소</span><span class="sxs-lookup"><span data-stu-id="3e0fe-117">Address third line</span></span>

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

### <span data-ttu-id="3e0fe-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e0fe-118">-AsJob</span></span>
<span data-ttu-id="3e0fe-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3e0fe-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e0fe-120">-City</span><span class="sxs-lookup"><span data-stu-id="3e0fe-120">-City</span></span>
<span data-ttu-id="3e0fe-121">시의 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-121">Name of the City</span></span>

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

### <span data-ttu-id="3e0fe-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="3e0fe-122">-CompanyName</span></span>
<span data-ttu-id="3e0fe-123">회사의 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-123">Name of the company</span></span>

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

### <span data-ttu-id="3e0fe-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="3e0fe-124">-ContactPerson</span></span>
<span data-ttu-id="3e0fe-125">연락처 사람의 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-125">Name of the contact person</span></span>

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

### <span data-ttu-id="3e0fe-126">-Country</span><span class="sxs-lookup"><span data-stu-id="3e0fe-126">-Country</span></span>
<span data-ttu-id="3e0fe-127">국가 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-127">Name of the Country</span></span>

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

### <span data-ttu-id="3e0fe-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0fe-128">-DefaultProfile</span></span>
<span data-ttu-id="3e0fe-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e0fe-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3e0fe-130">-DeviceName</span></span>
<span data-ttu-id="3e0fe-131">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-131">Resource Name</span></span>

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

### <span data-ttu-id="3e0fe-132">-Email</span><span class="sxs-lookup"><span data-stu-id="3e0fe-132">-Email</span></span>
<span data-ttu-id="3e0fe-133">업데이트를 받을 전자 메일 목록, 최대 10개 전자 메일 수락</span><span class="sxs-lookup"><span data-stu-id="3e0fe-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="3e0fe-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="3e0fe-134">-Phone</span></span>
<span data-ttu-id="3e0fe-135">연락처 사람의 전화 번호</span><span class="sxs-lookup"><span data-stu-id="3e0fe-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="3e0fe-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="3e0fe-136">-PostalCode</span></span>
<span data-ttu-id="3e0fe-137">주소의 우편 번호</span><span class="sxs-lookup"><span data-stu-id="3e0fe-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="3e0fe-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0fe-138">-ResourceGroupName</span></span>
<span data-ttu-id="3e0fe-139">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-139">Resource Group Name</span></span>

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

### <span data-ttu-id="3e0fe-140">-State</span><span class="sxs-lookup"><span data-stu-id="3e0fe-140">-State</span></span>
<span data-ttu-id="3e0fe-141">상태의 이름</span><span class="sxs-lookup"><span data-stu-id="3e0fe-141">Name of the State</span></span>

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

### <span data-ttu-id="3e0fe-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e0fe-142">-Confirm</span></span>
<span data-ttu-id="3e0fe-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e0fe-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e0fe-144">-WhatIf</span></span>
<span data-ttu-id="3e0fe-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3e0fe-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e0fe-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e0fe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0fe-147">CommonParameters</span></span>
<span data-ttu-id="3e0fe-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0fe-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e0fe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0fe-150">입력</span><span class="sxs-lookup"><span data-stu-id="3e0fe-150">INPUTS</span></span>

### <span data-ttu-id="3e0fe-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3e0fe-151">System.String</span></span>

## <span data-ttu-id="3e0fe-152">출력</span><span class="sxs-lookup"><span data-stu-id="3e0fe-152">OUTPUTS</span></span>

### <span data-ttu-id="3e0fe-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="3e0fe-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="3e0fe-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e0fe-154">NOTES</span></span>

## <span data-ttu-id="3e0fe-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e0fe-155">RELATED LINKS</span></span>
