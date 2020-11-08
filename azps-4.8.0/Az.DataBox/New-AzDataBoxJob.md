---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214595"
---
# <span data-ttu-id="19a84-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="19a84-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="19a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a84-102">SYNOPSIS</span></span>
<span data-ttu-id="19a84-103">지정 된 매개 변수를 사용 하 여 새 databox 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="19a84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19a84-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19a84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19a84-105">DESCRIPTION</span></span>
<span data-ttu-id="19a84-106">**새 AzDataBoxJob** cmdlet은 작업을 만드는 데 필요한 세부 정보를 지정 하 여 새 databox 작업을 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="19a84-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19a84-107">EXAMPLES</span></span>

### <span data-ttu-id="19a84-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="19a84-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="19a84-109">Cmdlet은 필요한 모든 매개 변수와 일부 선택적 매개 변수를 가져와 databox 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="19a84-110">변수</span><span class="sxs-lookup"><span data-stu-id="19a84-110">PARAMETERS</span></span>

### <span data-ttu-id="19a84-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="19a84-111">-AddressType</span></span>
<span data-ttu-id="19a84-112">주소 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-112">Type of Address.</span></span> <span data-ttu-id="19a84-113">사용 가능한 값: AddressType (기본값), AddressType, AddressType</span><span class="sxs-lookup"><span data-stu-id="19a84-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="19a84-114">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="19a84-114">-City</span></span>
<span data-ttu-id="19a84-115">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-115">Name of the City.</span></span> <span data-ttu-id="19a84-116">Ex: 샌프란시스코</span><span class="sxs-lookup"><span data-stu-id="19a84-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="19a84-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="19a84-117">-CompanyName</span></span>
<span data-ttu-id="19a84-118">회사 이름</span><span class="sxs-lookup"><span data-stu-id="19a84-118">Name of the company</span></span>

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

### <span data-ttu-id="19a84-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="19a84-119">-ContactName</span></span>
<span data-ttu-id="19a84-120">연락처 이름</span><span class="sxs-lookup"><span data-stu-id="19a84-120">Contact Name</span></span>

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

### <span data-ttu-id="19a84-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="19a84-121">-CountryCode</span></span>
<span data-ttu-id="19a84-122">국가 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-122">Country Code.</span></span> <span data-ttu-id="19a84-123">예: US</span><span class="sxs-lookup"><span data-stu-id="19a84-123">Ex: US</span></span>

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

### <span data-ttu-id="19a84-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="19a84-124">-DataBoxType</span></span>
<span data-ttu-id="19a84-125">Databox의 Sku 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-125">Sku type of Databox.</span></span>  <span data-ttu-id="19a84-126">사용 가능한 값: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="19a84-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="19a84-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a84-127">-DefaultProfile</span></span>
<span data-ttu-id="19a84-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19a84-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="19a84-129">-EmailId</span></span>
<span data-ttu-id="19a84-130">EmailIds 목록을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="19a84-131">적어도 1 개는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="19a84-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="19a84-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="19a84-133">DataBoxDisk order의 경우 테라바이트 단위로 예상 데이터를 지정 하는 것이 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="19a84-134">-위치</span><span class="sxs-lookup"><span data-stu-id="19a84-134">-Location</span></span>
<span data-ttu-id="19a84-135">구독 위치</span><span class="sxs-lookup"><span data-stu-id="19a84-135">Location of the subscription</span></span>

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

### <span data-ttu-id="19a84-136">-이름</span><span class="sxs-lookup"><span data-stu-id="19a84-136">-Name</span></span>
<span data-ttu-id="19a84-137">만들 databox 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="19a84-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="19a84-138">-PhoneNumber</span></span>
<span data-ttu-id="19a84-139">연락처 번호</span><span class="sxs-lookup"><span data-stu-id="19a84-139">Contact Number</span></span> 

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

### <span data-ttu-id="19a84-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="19a84-140">-PostalCode</span></span>
<span data-ttu-id="19a84-141">우편 번호</span><span class="sxs-lookup"><span data-stu-id="19a84-141">Postal Code</span></span>

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

### <span data-ttu-id="19a84-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a84-142">-ResourceGroupName</span></span>
<span data-ttu-id="19a84-143">Databox 작업을 만들어야 하는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="19a84-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="19a84-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="19a84-145">시/도 코드를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-145">Input the state or province code.</span></span> <span data-ttu-id="19a84-146">CA-캘리포니아와 좋아합니다. FL-플로리다 신규 서울 특별시</span><span class="sxs-lookup"><span data-stu-id="19a84-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="19a84-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="19a84-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="19a84-148">저장소 계정의 리소스 Id 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="19a84-149">적어도 1 개는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="19a84-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="19a84-150">-StreetAddress1</span></span>
<span data-ttu-id="19a84-151">주소란</span><span class="sxs-lookup"><span data-stu-id="19a84-151">Street Address</span></span>

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

### <span data-ttu-id="19a84-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="19a84-152">-StreetAddress2</span></span>
<span data-ttu-id="19a84-153">추가 주소</span><span class="sxs-lookup"><span data-stu-id="19a84-153">Additional Street Address</span></span>

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

### <span data-ttu-id="19a84-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="19a84-154">-StreetAddress3</span></span>
<span data-ttu-id="19a84-155">추가 주소</span><span class="sxs-lookup"><span data-stu-id="19a84-155">Additional Street Address</span></span>

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

### <span data-ttu-id="19a84-156">-확인</span><span class="sxs-lookup"><span data-stu-id="19a84-156">-Confirm</span></span>
<span data-ttu-id="19a84-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19a84-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19a84-158">-WhatIf</span></span>
<span data-ttu-id="19a84-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19a84-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19a84-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a84-161">CommonParameters</span></span>
<span data-ttu-id="19a84-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19a84-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a84-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19a84-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a84-164">입력</span><span class="sxs-lookup"><span data-stu-id="19a84-164">INPUTS</span></span>

### <span data-ttu-id="19a84-165">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="19a84-165">System.String[]</span></span>

## <span data-ttu-id="19a84-166">출력</span><span class="sxs-lookup"><span data-stu-id="19a84-166">OUTPUTS</span></span>

### <span data-ttu-id="19a84-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="19a84-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="19a84-168">상속자</span><span class="sxs-lookup"><span data-stu-id="19a84-168">NOTES</span></span>

## <span data-ttu-id="19a84-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19a84-169">RELATED LINKS</span></span>
