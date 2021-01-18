---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495711"
---
# <span data-ttu-id="2ad6c-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="2ad6c-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="2ad6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad6c-103">지정된 매개 변수를 사용하여 새 데이터 상자 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="2ad6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ad6c-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad6c-105">설명</span><span class="sxs-lookup"><span data-stu-id="2ad6c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad6c-106">**New-AzDataBoxJob** cmdlet은 작업을 만드는 데 필요한 세부 정보를 지정하여 새 데이터 상자 작업을 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="2ad6c-107">예제</span><span class="sxs-lookup"><span data-stu-id="2ad6c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ad6c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ad6c-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="2ad6c-109">cmdlet은 데이터 상자 작업을 만드는 데 필요한 모든 매개 변수 및 일부 선택적 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="2ad6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ad6c-110">PARAMETERS</span></span>

### <span data-ttu-id="2ad6c-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="2ad6c-111">-AddressType</span></span>
<span data-ttu-id="2ad6c-112">주소 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-112">Type of Address.</span></span> <span data-ttu-id="2ad6c-113">사용 가능한 값: AddressType.None(기본값), AddressType.Commercial, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="2ad6c-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad6c-114">-City</span><span class="sxs-lookup"><span data-stu-id="2ad6c-114">-City</span></span>
<span data-ttu-id="2ad6c-115">시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-115">Name of the City.</span></span> <span data-ttu-id="2ad6c-116">예: 샌프란시스코</span><span class="sxs-lookup"><span data-stu-id="2ad6c-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="2ad6c-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="2ad6c-117">-CompanyName</span></span>
<span data-ttu-id="2ad6c-118">회사의 이름</span><span class="sxs-lookup"><span data-stu-id="2ad6c-118">Name of the company</span></span>

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

### <span data-ttu-id="2ad6c-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="2ad6c-119">-ContactName</span></span>
<span data-ttu-id="2ad6c-120">연락처 이름</span><span class="sxs-lookup"><span data-stu-id="2ad6c-120">Contact Name</span></span>

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

### <span data-ttu-id="2ad6c-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="2ad6c-121">-CountryCode</span></span>
<span data-ttu-id="2ad6c-122">국가 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-122">Country Code.</span></span> <span data-ttu-id="2ad6c-123">예: 미국</span><span class="sxs-lookup"><span data-stu-id="2ad6c-123">Ex: US</span></span>

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

### <span data-ttu-id="2ad6c-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="2ad6c-124">-DataBoxType</span></span>
<span data-ttu-id="2ad6c-125">Databox의 SKU 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-125">Sku type of Databox.</span></span>  <span data-ttu-id="2ad6c-126">사용 가능한 값: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="2ad6c-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad6c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad6c-127">-DefaultProfile</span></span>
<span data-ttu-id="2ad6c-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad6c-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="2ad6c-129">-EmailId</span></span>
<span data-ttu-id="2ad6c-130">EmailId 목록은 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="2ad6c-131">Atleast one은 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="2ad6c-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="2ad6c-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="2ad6c-133">DataBoxDisk 순서의 경우 예상되는 데이터를 테라바이트로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad6c-134">-Location</span><span class="sxs-lookup"><span data-stu-id="2ad6c-134">-Location</span></span>
<span data-ttu-id="2ad6c-135">구독의 위치</span><span class="sxs-lookup"><span data-stu-id="2ad6c-135">Location of the subscription</span></span>

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

### <span data-ttu-id="2ad6c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="2ad6c-136">-Name</span></span>
<span data-ttu-id="2ad6c-137">만들 데이터 상자 작업의 이름</span><span class="sxs-lookup"><span data-stu-id="2ad6c-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="2ad6c-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2ad6c-138">-PhoneNumber</span></span>
<span data-ttu-id="2ad6c-139">연락처 번호</span><span class="sxs-lookup"><span data-stu-id="2ad6c-139">Contact Number</span></span> 

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

### <span data-ttu-id="2ad6c-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="2ad6c-140">-PostalCode</span></span>
<span data-ttu-id="2ad6c-141">우편 번호</span><span class="sxs-lookup"><span data-stu-id="2ad6c-141">Postal Code</span></span>

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

### <span data-ttu-id="2ad6c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad6c-142">-ResourceGroupName</span></span>
<span data-ttu-id="2ad6c-143">데이터 상자 작업을 만들어야 하는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="2ad6c-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="2ad6c-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="2ad6c-145">시 또는 도 코드를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-145">Input the state or province code.</span></span> <span data-ttu-id="2ad6c-146">CA와 마찬가지로 - 캘리포니아; FL - 플로리다; NY - 뉴욕</span><span class="sxs-lookup"><span data-stu-id="2ad6c-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="2ad6c-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2ad6c-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="2ad6c-148">저장소 계정의 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="2ad6c-149">Atleast는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad6c-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="2ad6c-150">-StreetAddress1</span></span>
<span data-ttu-id="2ad6c-151">주소</span><span class="sxs-lookup"><span data-stu-id="2ad6c-151">Street Address</span></span>

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

### <span data-ttu-id="2ad6c-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="2ad6c-152">-StreetAddress2</span></span>
<span data-ttu-id="2ad6c-153">추가 주소</span><span class="sxs-lookup"><span data-stu-id="2ad6c-153">Additional Street Address</span></span>

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

### <span data-ttu-id="2ad6c-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="2ad6c-154">-StreetAddress3</span></span>
<span data-ttu-id="2ad6c-155">추가 주소</span><span class="sxs-lookup"><span data-stu-id="2ad6c-155">Additional Street Address</span></span>

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

### <span data-ttu-id="2ad6c-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ad6c-156">-Confirm</span></span>
<span data-ttu-id="2ad6c-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad6c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad6c-158">-WhatIf</span></span>
<span data-ttu-id="2ad6c-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2ad6c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ad6c-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad6c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad6c-161">CommonParameters</span></span>
<span data-ttu-id="2ad6c-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad6c-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ad6c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad6c-164">입력</span><span class="sxs-lookup"><span data-stu-id="2ad6c-164">INPUTS</span></span>

### <span data-ttu-id="2ad6c-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2ad6c-165">System.String[]</span></span>

## <span data-ttu-id="2ad6c-166">출력</span><span class="sxs-lookup"><span data-stu-id="2ad6c-166">OUTPUTS</span></span>

### <span data-ttu-id="2ad6c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="2ad6c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="2ad6c-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ad6c-168">NOTES</span></span>

## <span data-ttu-id="2ad6c-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ad6c-169">RELATED LINKS</span></span>
