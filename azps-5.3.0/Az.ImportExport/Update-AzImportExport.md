---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495405"
---
# <span data-ttu-id="3b6e6-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="3b6e6-101">Update-AzImportExport</span></span>

## <span data-ttu-id="3b6e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6e6-103">작업의 특정 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="3b6e6-104">이 작업을 호출하여 Import/Export 서비스에 가져오기 또는 내보내기 작업이 있는 하드 드라이브가 Microsoft 데이터 센터로 배송된 경우를 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="3b6e6-105">기존 작업을 취소하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="3b6e6-106">구문</span><span class="sxs-lookup"><span data-stu-id="3b6e6-106">SYNTAX</span></span>

### <span data-ttu-id="3b6e6-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="3b6e6-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b6e6-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b6e6-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b6e6-109">설명</span><span class="sxs-lookup"><span data-stu-id="3b6e6-109">DESCRIPTION</span></span>
<span data-ttu-id="3b6e6-110">작업의 특정 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="3b6e6-111">이 작업을 호출하여 Import/Export 서비스에 가져오기 또는 내보내기 작업이 있는 하드 드라이브가 Microsoft 데이터 센터로 배송된 경우를 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="3b6e6-112">기존 작업을 취소하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="3b6e6-113">예제</span><span class="sxs-lookup"><span data-stu-id="3b6e6-113">EXAMPLES</span></span>

### <span data-ttu-id="3b6e6-114">예제 1: 리소스 그룹 및 서버 이름으로 ImportExport 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="3b6e6-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3b6e6-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 ImportExport 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="3b6e6-116">예제 2: ID로 ImportExport 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="3b6e6-117">이 cmdlet은 ID에 의해 ImportExport 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="3b6e6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b6e6-118">PARAMETERS</span></span>

### <span data-ttu-id="3b6e6-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3b6e6-119">-AcceptLanguage</span></span>
<span data-ttu-id="3b6e6-120">응답에 대한 기본 설정 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3b6e6-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="3b6e6-121">-BackupDriveManifest</span></span>
<span data-ttu-id="3b6e6-122">드라이브의 매니페스트 파일을 블록 Blob에 복사해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="3b6e6-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="3b6e6-123">-CancelRequested</span></span>
<span data-ttu-id="3b6e6-124">지정된 경우 값은 true가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-124">If specified, the value must be true.</span></span>
<span data-ttu-id="3b6e6-125">서비스가 작업을 취소하려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="3b6e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6e6-126">-DefaultProfile</span></span>
<span data-ttu-id="3b6e6-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="3b6e6-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="3b6e6-129">가져오기 또는 내보내기 드라이브를 배송하는 데 사용되는 운송업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="3b6e6-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="3b6e6-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="3b6e6-131">패키지에 포함된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="3b6e6-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="3b6e6-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="3b6e6-133">패키지가 배송된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="3b6e6-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="3b6e6-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="3b6e6-135">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="3b6e6-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="3b6e6-136">-DriveList</span></span>
<span data-ttu-id="3b6e6-137">작업을 구성하는 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="3b6e6-138">생성하기 위해 DRIVELIST 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b6e6-139">-InputObject</span></span>
<span data-ttu-id="3b6e6-140">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="3b6e6-141">-LogLevel</span></span>
<span data-ttu-id="3b6e6-142">오류 로깅 또는 오류 표시 로깅을 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="3b6e6-143">-Name</span><span class="sxs-lookup"><span data-stu-id="3b6e6-143">-Name</span></span>
<span data-ttu-id="3b6e6-144">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6e6-145">-ResourceGroupName</span></span>
<span data-ttu-id="3b6e6-146">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="3b6e6-147">-ReturnAddressCity</span></span>
<span data-ttu-id="3b6e6-148">드라이브를 반환할 때 사용할 도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="3b6e6-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="3b6e6-150">드라이브를 반환할 때 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="3b6e6-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="3b6e6-152">반환된 드라이브의 받는 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="3b6e6-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="3b6e6-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="3b6e6-154">반환된 드라이브의 받는 사람의 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="3b6e6-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="3b6e6-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="3b6e6-156">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="3b6e6-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="3b6e6-158">하드 드라이브가 반환될 때 받는 사람의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="3b6e6-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="3b6e6-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="3b6e6-160">드라이브를 반환할 때 사용할 주 또는 도입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="3b6e6-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="3b6e6-162">드라이브를 반환할 때 사용할 도로 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="3b6e6-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="3b6e6-164">드라이브를 반환할 때 사용할 도로 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="3b6e6-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="3b6e6-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="3b6e6-166">운송업체를 통해 고객의 계정 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="3b6e6-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="3b6e6-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="3b6e6-168">운송업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-168">The carrier's name.</span></span>

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

### <span data-ttu-id="3b6e6-169">-State</span><span class="sxs-lookup"><span data-stu-id="3b6e6-169">-State</span></span>
<span data-ttu-id="3b6e6-170">지정된 경우 값은 가져오기/내보내기 서비스에 작업의 패키지가 배송된 것을 알려 주며 배송되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="3b6e6-171">ReturnAddress 및 DeliveryPackage 속성은 이 요청 또는 이전 요청에서 설정되어야 합니다. 그렇지 않으면 요청이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="3b6e6-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b6e6-172">-SubscriptionId</span></span>
<span data-ttu-id="3b6e6-173">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b6e6-174">-Tag</span></span>
<span data-ttu-id="3b6e6-175">작업으로 할당될 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6e6-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b6e6-176">-Confirm</span></span>
<span data-ttu-id="3b6e6-177">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b6e6-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6e6-178">-WhatIf</span></span>
<span data-ttu-id="3b6e6-179">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3b6e6-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6e6-180">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b6e6-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6e6-181">CommonParameters</span></span>
<span data-ttu-id="3b6e6-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6e6-183">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6e6-184">입력</span><span class="sxs-lookup"><span data-stu-id="3b6e6-184">INPUTS</span></span>

### <span data-ttu-id="3b6e6-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="3b6e6-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3b6e6-186">출력</span><span class="sxs-lookup"><span data-stu-id="3b6e6-186">OUTPUTS</span></span>

### <span data-ttu-id="3b6e6-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="3b6e6-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="3b6e6-188">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3b6e6-188">NOTES</span></span>

<span data-ttu-id="3b6e6-189">별칭</span><span class="sxs-lookup"><span data-stu-id="3b6e6-189">ALIASES</span></span>

<span data-ttu-id="3b6e6-190">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3b6e6-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b6e6-191">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b6e6-192">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b6e6-193">DRIVELIST <IDriveStatus[]>: 작업을 구성하는 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="3b6e6-194">`[BitLockerKey <String>]`: 드라이브를 암호화하는 데 사용되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="3b6e6-195">`[BytesSucceeded <Int64?>]`: 드라이브에 대해 성공적으로 전송된 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="3b6e6-196">`[CopyStatus <String>]`: 데이터 전송 프로세스에 대한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="3b6e6-197">이 필드는 드라이브가 전송 중 상태가 될 때까지 응답에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="3b6e6-198">`[DriveHeaderHash <String>]`: 드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="3b6e6-199">`[DriveId <String>]`: 드라이브의 하드웨어 일련 번호(공백 없이).</span><span class="sxs-lookup"><span data-stu-id="3b6e6-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="3b6e6-200">`[ErrorLogUri <String>]`: 데이터 전송 작업에 대한 오류 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="3b6e6-201">`[ManifestFile <String>]`: 드라이브에 있는 매니페스트 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="3b6e6-202">`[ManifestHash <String>]`: 드라이브에 있는 매니페스트 파일의 Base16 인코딩 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="3b6e6-203">`[ManifestUri <String>]`: 드라이브 매니페스트 파일이 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="3b6e6-204">`[PercentComplete <Int32?>]`: 드라이브에 대해 완료된 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="3b6e6-205">`[State <DriveState?>]`: 드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="3b6e6-206">`[VerboseLogUri <String>]`: 데이터 전송 작업에 대한 자세한 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="3b6e6-207">INPUTOBJECT: <IImportExportIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3b6e6-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b6e6-208">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3b6e6-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b6e6-209">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3b6e6-210">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3b6e6-211">예를 들어 미국 서부 또는 westus입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="3b6e6-212">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3b6e6-213">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6e6-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3b6e6-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b6e6-214">RELATED LINKS</span></span>

