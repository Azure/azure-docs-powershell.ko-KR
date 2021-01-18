---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495492"
---
# <span data-ttu-id="e4fb6-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e4fb6-101">New-AzImportExport</span></span>

## <span data-ttu-id="e4fb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fb6-103">새 작업을 생성하거나 지정된 구독에서 기존 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="e4fb6-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4fb6-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e4fb6-105">설명</span><span class="sxs-lookup"><span data-stu-id="e4fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fb6-106">새 작업을 생성하거나 지정된 구독에서 기존 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="e4fb6-107">예제</span><span class="sxs-lookup"><span data-stu-id="e4fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fb6-108">예제 1: 새 ImportExport 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="e4fb6-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="e4fb6-109">이러한 cmdlet은 새 ImportExport 작업을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="e4fb6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fb6-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e4fb6-111">-AcceptLanguage</span></span>
<span data-ttu-id="e4fb6-112">응답에 대한 기본 설정 언어를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="e4fb6-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="e4fb6-113">-BackupDriveManifest</span></span>
<span data-ttu-id="e4fb6-114">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-114">Default value is false.</span></span>
<span data-ttu-id="e4fb6-115">드라이브의 매니페스트 파일을 블록 Blob에 복사해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="e4fb6-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="e4fb6-116">-BlobListBlobPath</span></span>
<span data-ttu-id="e4fb6-117">Blob 경로 문자열의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb6-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="e4fb6-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="e4fb6-119">Blob-prefix 문자열의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb6-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="e4fb6-120">-CancelRequested</span></span>
<span data-ttu-id="e4fb6-121">요청을 제출하여 작업을 취소할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="e4fb6-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="e4fb6-122">-ClientTenantId</span></span>
<span data-ttu-id="e4fb6-123">요청을 하는 클라이언트의 테넌트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="e4fb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fb6-124">-DefaultProfile</span></span>
<span data-ttu-id="e4fb6-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4fb6-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="e4fb6-127">가져오기 또는 내보내기 드라이브를 배송하는 데 사용되는 운송업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="e4fb6-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="e4fb6-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="e4fb6-129">패키지에 포함된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="e4fb6-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="e4fb6-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="e4fb6-131">패키지가 배송된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="e4fb6-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="e4fb6-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="e4fb6-133">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="e4fb6-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="e4fb6-134">-DiagnosticsPath</span></span>
<span data-ttu-id="e4fb6-135">드라이브 매니페스트 파일의 복사 로그 및 백업(활성화된 경우)을 저장할 가상 Blob 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="e4fb6-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="e4fb6-136">-DriveList</span></span>
<span data-ttu-id="e4fb6-137">작업을 구성하는 최대 10개의 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="e4fb6-138">드라이브 목록은 가져오기 작업의 필수 요소입니다. 내보내기 작업의 경우 지정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="e4fb6-139">생성하기 위해 DRIVELIST 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4fb6-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="e4fb6-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="e4fb6-141">컨테이너 이름으로 시작하여 위에서 정의한 대로 Blob 경로 또는 Blob 경로의 목록을 포함하는 블록 Blob에 대한 상대 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="e4fb6-142">Blob이 루트 컨테이너에 있는 경우 URI는 루트 컨테이너로 $root.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="e4fb6-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="e4fb6-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="e4fb6-144">드라이브 공간이 부족하여 내보낼 수 없는 Blob 이름 목록이 포함된 블록 Blob을 지점으로 하는 Blob 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="e4fb6-145">모든 Blob을 성공적으로 내보낼 경우 이 요소는 응답에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="e4fb6-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="e4fb6-146">-JobType</span></span>
<span data-ttu-id="e4fb6-147">작업 유형</span><span class="sxs-lookup"><span data-stu-id="e4fb6-147">The type of job</span></span>

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

### <span data-ttu-id="e4fb6-148">-Location</span><span class="sxs-lookup"><span data-stu-id="e4fb6-148">-Location</span></span>
<span data-ttu-id="e4fb6-149">작업을 만들어야 하는 지원되는 Azure 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="e4fb6-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="e4fb6-150">-LogLevel</span></span>
<span data-ttu-id="e4fb6-151">기본값은 Error입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-151">Default value is Error.</span></span>
<span data-ttu-id="e4fb6-152">오류 로깅 또는 Verbose 로깅을 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="e4fb6-153">-Name</span><span class="sxs-lookup"><span data-stu-id="e4fb6-153">-Name</span></span>
<span data-ttu-id="e4fb6-154">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb6-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e4fb6-155">-PercentComplete</span></span>
<span data-ttu-id="e4fb6-156">작업 완료의 전체 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="e4fb6-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e4fb6-157">-ProvisioningState</span></span>
<span data-ttu-id="e4fb6-158">작업의 프로비전 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="e4fb6-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-159">-ResourceGroupName</span></span>
<span data-ttu-id="e4fb6-160">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유하게 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="e4fb6-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="e4fb6-161">-ReturnAddressCity</span></span>
<span data-ttu-id="e4fb6-162">드라이브를 반환할 때 사용할 도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e4fb6-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="e4fb6-164">드라이브를 반환할 때 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="e4fb6-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="e4fb6-166">반환된 드라이브의 받는 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="e4fb6-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="e4fb6-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="e4fb6-168">반환된 드라이브의 받는 사람의 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="e4fb6-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="e4fb6-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="e4fb6-170">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="e4fb6-172">하드 드라이브가 반환될 때 받는 사람의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="e4fb6-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="e4fb6-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="e4fb6-174">드라이브를 반환할 때 사용할 주 또는 도입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="e4fb6-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="e4fb6-176">드라이브를 반환할 때 사용할 도로 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="e4fb6-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="e4fb6-178">드라이브를 반환할 때 사용할 도로 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="e4fb6-180">가져오기 또는 내보내기 드라이브를 배송하는 데 사용되는 운송업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="e4fb6-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="e4fb6-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="e4fb6-182">패키지에 포함된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="e4fb6-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="e4fb6-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="e4fb6-184">패키지가 배송된 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="e4fb6-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="e4fb6-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="e4fb6-186">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="e4fb6-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="e4fb6-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="e4fb6-188">운송업체를 통해 고객의 계정 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="e4fb6-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="e4fb6-190">운송업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-190">The carrier's name.</span></span>

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

### <span data-ttu-id="e4fb6-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="e4fb6-191">-ShippingInformationCity</span></span>
<span data-ttu-id="e4fb6-192">드라이브를 반환할 때 사용할 도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e4fb6-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="e4fb6-194">드라이브를 반환할 때 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="e4fb6-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="e4fb6-196">반환된 드라이브의 받는 사람의 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="e4fb6-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="e4fb6-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="e4fb6-198">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="e4fb6-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="e4fb6-200">하드 드라이브가 반환될 때 받는 사람의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="e4fb6-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="e4fb6-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="e4fb6-202">드라이브를 반환할 때 사용할 주 또는 도입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="e4fb6-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="e4fb6-204">드라이브를 반환할 때 사용할 도로 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="e4fb6-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="e4fb6-206">드라이브를 반환할 때 사용할 도로 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="e4fb6-207">-State</span><span class="sxs-lookup"><span data-stu-id="e4fb6-207">-State</span></span>
<span data-ttu-id="e4fb6-208">작업의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-208">Current state of the job.</span></span>

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

### <span data-ttu-id="e4fb6-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4fb6-209">-StorageAccountId</span></span>
<span data-ttu-id="e4fb6-210">데이터를 가져오거나 내보낼 저장소 계정의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="e4fb6-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4fb6-211">-SubscriptionId</span></span>
<span data-ttu-id="e4fb6-212">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb6-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4fb6-213">-Tag</span></span>
<span data-ttu-id="e4fb6-214">작업을 할당할 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb6-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4fb6-215">-Confirm</span></span>
<span data-ttu-id="e4fb6-216">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4fb6-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4fb6-217">-WhatIf</span></span>
<span data-ttu-id="e4fb6-218">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e4fb6-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4fb6-219">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4fb6-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fb6-220">CommonParameters</span></span>
<span data-ttu-id="e4fb6-221">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fb6-222">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fb6-223">입력</span><span class="sxs-lookup"><span data-stu-id="e4fb6-223">INPUTS</span></span>

## <span data-ttu-id="e4fb6-224">출력</span><span class="sxs-lookup"><span data-stu-id="e4fb6-224">OUTPUTS</span></span>

### <span data-ttu-id="e4fb6-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="e4fb6-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="e4fb6-226">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4fb6-226">NOTES</span></span>

<span data-ttu-id="e4fb6-227">별칭</span><span class="sxs-lookup"><span data-stu-id="e4fb6-227">ALIASES</span></span>

<span data-ttu-id="e4fb6-228">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e4fb6-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4fb6-229">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4fb6-230">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4fb6-231">DRIVELIST <IDriveStatus[]>: 작업을 구성하는 최대 10개의 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="e4fb6-232">드라이브 목록은 가져오기 작업의 필수 요소입니다. 내보내기 작업의 경우 지정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="e4fb6-233">`[BitLockerKey <String>]`: 드라이브를 암호화하는 데 사용되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="e4fb6-234">`[BytesSucceeded <Int64?>]`: 드라이브에 대해 성공적으로 전송된 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="e4fb6-235">`[CopyStatus <String>]`: 데이터 전송 프로세스에 대한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="e4fb6-236">이 필드는 드라이브가 전송 중 상태가 될 때까지 응답에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="e4fb6-237">`[DriveHeaderHash <String>]`: 드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="e4fb6-238">`[DriveId <String>]`: 드라이브의 하드웨어 일련 번호(공백 없이).</span><span class="sxs-lookup"><span data-stu-id="e4fb6-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="e4fb6-239">`[ErrorLogUri <String>]`: 데이터 전송 작업에 대한 오류 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="e4fb6-240">`[ManifestFile <String>]`: 드라이브에 있는 매니페스트 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="e4fb6-241">`[ManifestHash <String>]`: 드라이브에 있는 매니페스트 파일의 Base16 인코딩 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="e4fb6-242">`[ManifestUri <String>]`: 드라이브 매니페스트 파일이 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="e4fb6-243">`[PercentComplete <Int32?>]`: 드라이브에 대해 완료된 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="e4fb6-244">`[State <DriveState?>]`: 드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="e4fb6-245">`[VerboseLogUri <String>]`: 데이터 전송 작업에 대한 자세한 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb6-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="e4fb6-246">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4fb6-246">RELATED LINKS</span></span>

