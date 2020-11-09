---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303992"
---
# <span data-ttu-id="a92fe-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a92fe-101">New-AzImportExport</span></span>

## <span data-ttu-id="a92fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a92fe-103">지정 된 구독에서 새 작업을 만들거나 기존 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="a92fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a92fe-104">SYNTAX</span></span>

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

## <span data-ttu-id="a92fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a92fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a92fe-106">지정 된 구독에서 새 작업을 만들거나 기존 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="a92fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a92fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a92fe-108">예제 1: 새 ImportExport 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="a92fe-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a92fe-109">이러한 cmdlet은 새 ImportExport 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="a92fe-110">변수</span><span class="sxs-lookup"><span data-stu-id="a92fe-110">PARAMETERS</span></span>

### <span data-ttu-id="a92fe-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a92fe-111">-AcceptLanguage</span></span>
<span data-ttu-id="a92fe-112">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="a92fe-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="a92fe-113">-BackupDriveManifest</span></span>
<span data-ttu-id="a92fe-114">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-114">Default value is false.</span></span>
<span data-ttu-id="a92fe-115">드라이브의 매니페스트 파일을 blob을 차단 하도록 복사할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="a92fe-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="a92fe-116">-BlobListBlobPath</span></span>
<span data-ttu-id="a92fe-117">Blob 경로 문자열의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="a92fe-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="a92fe-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="a92fe-119">Blob 접두사 문자열의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="a92fe-120">-CancelRequested 됨</span><span class="sxs-lookup"><span data-stu-id="a92fe-120">-CancelRequested</span></span>
<span data-ttu-id="a92fe-121">작업을 취소 하기 위해 요청이 제출 되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="a92fe-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="a92fe-122">-ClientTenantId</span></span>
<span data-ttu-id="a92fe-123">요청을 보내는 클라이언트의 테 넌 트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="a92fe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92fe-124">-DefaultProfile</span></span>
<span data-ttu-id="a92fe-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a92fe-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="a92fe-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="a92fe-127">가져오기 또는 내보내기 드라이브를 제공 하는 데 사용 되는 통신 회사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="a92fe-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="a92fe-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="a92fe-129">패키지에 포함 된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="a92fe-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="a92fe-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="a92fe-131">패키지가 배송 되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="a92fe-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="a92fe-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="a92fe-133">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="a92fe-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="a92fe-134">-DiagnosticsPath</span></span>
<span data-ttu-id="a92fe-135">복사본을 로그 하 고 드라이브 매니페스트 파일 (사용 가능)을 백업 하는 가상 blob 디렉터리를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="a92fe-136">-드라이브 목록</span><span class="sxs-lookup"><span data-stu-id="a92fe-136">-DriveList</span></span>
<span data-ttu-id="a92fe-137">작업을 구성 하는 최대 10 개의 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="a92fe-138">드라이브 목록은 가져오기 작업에 대 한 필수 요소입니다. 내보내기 작업에 대해 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="a92fe-139">생성 하려면 드라이브 목록 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="a92fe-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="a92fe-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="a92fe-141">컨테이너 이름부터 앞에 정의 된 blob 경로 또는 blob 경로 접두사 목록이 포함 된 block blob에 대 한 상대 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="a92fe-142">Blob이 루트 컨테이너에 있는 경우 URI는 $root으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="a92fe-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="a92fe-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="a92fe-144">드라이브 공간 부족으로 내보내지 않은 blob 이름 목록이 포함 된 block blob을 가리키는 blob 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="a92fe-145">모든 blob을 성공적으로 내보내면이 요소가 응답에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="a92fe-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="a92fe-146">-JobType</span></span>
<span data-ttu-id="a92fe-147">작업 유형</span><span class="sxs-lookup"><span data-stu-id="a92fe-147">The type of job</span></span>

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

### <span data-ttu-id="a92fe-148">-위치</span><span class="sxs-lookup"><span data-stu-id="a92fe-148">-Location</span></span>
<span data-ttu-id="a92fe-149">작업을 만들어야 하는 지원 되는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="a92fe-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="a92fe-150">-LogLevel</span></span>
<span data-ttu-id="a92fe-151">기본값은 오류입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-151">Default value is Error.</span></span>
<span data-ttu-id="a92fe-152">오류 로깅 또는 자세한 로깅이 사용 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="a92fe-153">-이름</span><span class="sxs-lookup"><span data-stu-id="a92fe-153">-Name</span></span>
<span data-ttu-id="a92fe-154">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="a92fe-155">-완료율</span><span class="sxs-lookup"><span data-stu-id="a92fe-155">-PercentComplete</span></span>
<span data-ttu-id="a92fe-156">작업에 대 한 전체 백분율이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="a92fe-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="a92fe-157">-ProvisioningState</span></span>
<span data-ttu-id="a92fe-158">작업의 프로 비전 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="a92fe-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92fe-159">-ResourceGroupName</span></span>
<span data-ttu-id="a92fe-160">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="a92fe-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="a92fe-161">-ReturnAddressCity</span></span>
<span data-ttu-id="a92fe-162">드라이브를 반환할 때 사용할 구/군/시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a92fe-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="a92fe-164">드라이브를 반환 하는 데 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="a92fe-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="a92fe-166">반환 된 드라이브의 받는 사람에 대 한 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a92fe-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="a92fe-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="a92fe-168">반환 된 드라이브의 받는 사람에 대 한 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a92fe-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="a92fe-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="a92fe-170">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="a92fe-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="a92fe-172">하드 드라이브가 반환 될 때이를 받을 수신자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="a92fe-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="a92fe-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="a92fe-174">드라이브를 반환할 때 사용할 시/도입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="a92fe-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="a92fe-176">드라이브를 반환할 때 사용할 거리 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="a92fe-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="a92fe-178">드라이브를 반환할 때 사용할 거리 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="a92fe-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="a92fe-180">가져오기 또는 내보내기 드라이브를 제공 하는 데 사용 되는 통신 회사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="a92fe-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="a92fe-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="a92fe-182">패키지에 포함 된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="a92fe-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="a92fe-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="a92fe-184">패키지가 배송 되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="a92fe-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="a92fe-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="a92fe-186">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="a92fe-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="a92fe-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="a92fe-188">통신 회사와 고객의 계정 번호</span><span class="sxs-lookup"><span data-stu-id="a92fe-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="a92fe-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="a92fe-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="a92fe-190">통신 회사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-190">The carrier's name.</span></span>

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

### <span data-ttu-id="a92fe-191">-배송 도시</span><span class="sxs-lookup"><span data-stu-id="a92fe-191">-ShippingInformationCity</span></span>
<span data-ttu-id="a92fe-192">드라이브를 반환할 때 사용할 구/군/시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a92fe-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="a92fe-194">드라이브를 반환 하는 데 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-195">-배송 전화 번호</span><span class="sxs-lookup"><span data-stu-id="a92fe-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="a92fe-196">반환 된 드라이브의 받는 사람에 대 한 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a92fe-197">-배송 하는 Postalcode</span><span class="sxs-lookup"><span data-stu-id="a92fe-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="a92fe-198">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="a92fe-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="a92fe-200">하드 드라이브가 반환 될 때이를 받을 수신자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="a92fe-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="a92fe-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="a92fe-202">드라이브를 반환할 때 사용할 시/도입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="a92fe-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="a92fe-204">드라이브를 반환할 때 사용할 거리 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="a92fe-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="a92fe-206">드라이브를 반환할 때 사용할 거리 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a92fe-207">-상태</span><span class="sxs-lookup"><span data-stu-id="a92fe-207">-State</span></span>
<span data-ttu-id="a92fe-208">작업의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-208">Current state of the job.</span></span>

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

### <span data-ttu-id="a92fe-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a92fe-209">-StorageAccountId</span></span>
<span data-ttu-id="a92fe-210">데이터를 가져오거나 내보낼 저장소 계정의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="a92fe-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a92fe-211">-SubscriptionId</span></span>
<span data-ttu-id="a92fe-212">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="a92fe-213">태그</span><span class="sxs-lookup"><span data-stu-id="a92fe-213">-Tag</span></span>
<span data-ttu-id="a92fe-214">작업에 할당 되는 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="a92fe-215">-확인</span><span class="sxs-lookup"><span data-stu-id="a92fe-215">-Confirm</span></span>
<span data-ttu-id="a92fe-216">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92fe-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92fe-217">-WhatIf</span></span>
<span data-ttu-id="a92fe-218">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92fe-219">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92fe-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92fe-220">CommonParameters</span></span>
<span data-ttu-id="a92fe-221">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92fe-222">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a92fe-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92fe-223">입력</span><span class="sxs-lookup"><span data-stu-id="a92fe-223">INPUTS</span></span>

## <span data-ttu-id="a92fe-224">출력</span><span class="sxs-lookup"><span data-stu-id="a92fe-224">OUTPUTS</span></span>

### <span data-ttu-id="a92fe-225">Api20161101 내보내기. i i a PowerShell. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="a92fe-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="a92fe-226">상속자</span><span class="sxs-lookup"><span data-stu-id="a92fe-226">NOTES</span></span>

<span data-ttu-id="a92fe-227">별칭과</span><span class="sxs-lookup"><span data-stu-id="a92fe-227">ALIASES</span></span>

<span data-ttu-id="a92fe-228">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a92fe-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a92fe-229">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a92fe-230">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a92fe-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a92fe-231">드라이브 목록 <IDriveStatus [] >: 작업을 구성 하는 최대 10 개의 드라이브가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="a92fe-232">드라이브 목록은 가져오기 작업에 대 한 필수 요소입니다. 내보내기 작업에 대해 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="a92fe-233">`[BitLockerKey <String>]`: 드라이브를 암호화 하는 데 사용 되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="a92fe-234">`[BytesSucceeded <Int64?>]`: 드라이브에 대 한 바이트가 전송 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="a92fe-235">`[CopyStatus <String>]`: 데이터 전송 프로세스에 대 한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="a92fe-236">이 필드는 드라이브가 전송 상태에 있을 때까지 응답에 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="a92fe-237">`[DriveHeaderHash <String>]`: 드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="a92fe-238">`[DriveId <String>]`: 드라이브의 하드웨어 일련 번호 (공백 없음).</span><span class="sxs-lookup"><span data-stu-id="a92fe-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="a92fe-239">`[ErrorLogUri <String>]`: 데이터 전송 작업에 대 한 오류 로그를 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="a92fe-240">`[ManifestFile <String>]`: 드라이브의 매니페스트 파일에 대 한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="a92fe-241">`[ManifestHash <String>]`: 드라이브의 매니페스트 파일에 대 한 Base16 인코딩된 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="a92fe-242">`[ManifestUri <String>]`: 드라이브 매니페스트 파일을 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="a92fe-243">`[PercentComplete <Int32?>]`: 드라이브의 백분율이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="a92fe-244">`[State <DriveState?>]`: 드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="a92fe-245">`[VerboseLogUri <String>]`: 데이터 전송 작업에 대 한 자세한 로그를 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a92fe-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="a92fe-246">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a92fe-246">RELATED LINKS</span></span>

