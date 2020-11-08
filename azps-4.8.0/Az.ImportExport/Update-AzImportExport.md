---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212213"
---
# <span data-ttu-id="1ec81-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="1ec81-101">Update-AzImportExport</span></span>

## <span data-ttu-id="1ec81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec81-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec81-103">작업의 특정 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="1ec81-104">이 작업을 호출 하 여 가져오기/내보내기 서비스에 가져오거나 내보내기 작업을 수행 하는 하드 드라이브가 Microsoft 데이터 센터로 제공 되었음을 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="1ec81-105">이를 사용 하 여 기존 작업을 취소할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="1ec81-106">구문과</span><span class="sxs-lookup"><span data-stu-id="1ec81-106">SYNTAX</span></span>

### <span data-ttu-id="1ec81-107">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ec81-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="1ec81-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ec81-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="1ec81-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1ec81-109">DESCRIPTION</span></span>
<span data-ttu-id="1ec81-110">작업의 특정 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="1ec81-111">이 작업을 호출 하 여 가져오기/내보내기 서비스에 가져오거나 내보내기 작업을 수행 하는 하드 드라이브가 Microsoft 데이터 센터로 제공 되었음을 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="1ec81-112">이를 사용 하 여 기존 작업을 취소할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="1ec81-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1ec81-113">EXAMPLES</span></span>

### <span data-ttu-id="1ec81-114">예제 1: 리소스 그룹 및 서버 이름에의 한 ImportExport 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="1ec81-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="1ec81-115">이 cmdlet은 리소스 그룹별 ImportExport 작업을 업데이트 하 고, 서버 이름을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="1ec81-116">예제 2: id를 기준으로 가져오기 내보내기 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="1ec81-117">이 cmdlet은 id를 기준으로 ImportExport 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="1ec81-118">변수</span><span class="sxs-lookup"><span data-stu-id="1ec81-118">PARAMETERS</span></span>

### <span data-ttu-id="1ec81-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1ec81-119">-AcceptLanguage</span></span>
<span data-ttu-id="1ec81-120">응답의 기본 언어를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="1ec81-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="1ec81-121">-BackupDriveManifest</span></span>
<span data-ttu-id="1ec81-122">드라이브의 매니페스트 파일을 blob을 차단 하도록 복사할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="1ec81-123">-CancelRequested 됨</span><span class="sxs-lookup"><span data-stu-id="1ec81-123">-CancelRequested</span></span>
<span data-ttu-id="1ec81-124">지정 된 경우 값이 true 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-124">If specified, the value must be true.</span></span>
<span data-ttu-id="1ec81-125">서비스가 작업을 취소 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="1ec81-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec81-126">-DefaultProfile</span></span>
<span data-ttu-id="1ec81-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec81-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="1ec81-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="1ec81-129">가져오기 또는 내보내기 드라이브를 제공 하는 데 사용 되는 통신 회사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="1ec81-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="1ec81-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="1ec81-131">패키지에 포함 된 드라이브 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="1ec81-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="1ec81-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="1ec81-133">패키지가 배송 되는 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="1ec81-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="1ec81-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="1ec81-135">패키지의 추적 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="1ec81-136">-드라이브 목록</span><span class="sxs-lookup"><span data-stu-id="1ec81-136">-DriveList</span></span>
<span data-ttu-id="1ec81-137">작업을 구성 하는 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="1ec81-138">생성 하려면 드라이브 목록 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ec81-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec81-139">-InputObject</span></span>
<span data-ttu-id="1ec81-140">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ec81-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="1ec81-141">-LogLevel</span></span>
<span data-ttu-id="1ec81-142">오류 로깅 또는 자세한 로깅이 설정 되었는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="1ec81-143">-이름</span><span class="sxs-lookup"><span data-stu-id="1ec81-143">-Name</span></span>
<span data-ttu-id="1ec81-144">가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="1ec81-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec81-145">-ResourceGroupName</span></span>
<span data-ttu-id="1ec81-146">리소스 그룹 이름은 사용자 구독 내의 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="1ec81-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="1ec81-147">-ReturnAddressCity</span></span>
<span data-ttu-id="1ec81-148">드라이브를 반환할 때 사용할 구/군/시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="1ec81-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="1ec81-150">드라이브를 반환 하는 데 사용할 국가 또는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="1ec81-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="1ec81-152">반환 된 드라이브의 받는 사람에 대 한 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="1ec81-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="1ec81-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="1ec81-154">반환 된 드라이브의 받는 사람에 대 한 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="1ec81-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="1ec81-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="1ec81-156">드라이브를 반환할 때 사용할 우편 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="1ec81-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="1ec81-158">하드 드라이브가 반환 될 때이를 받을 수신자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="1ec81-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="1ec81-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="1ec81-160">드라이브를 반환할 때 사용할 시/도입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="1ec81-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="1ec81-162">드라이브를 반환할 때 사용할 거리 주소의 첫 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="1ec81-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="1ec81-164">드라이브를 반환할 때 사용할 거리 주소의 두 번째 줄입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="1ec81-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="1ec81-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="1ec81-166">통신 회사와 고객의 계정 번호</span><span class="sxs-lookup"><span data-stu-id="1ec81-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="1ec81-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="1ec81-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="1ec81-168">통신 회사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-168">The carrier's name.</span></span>

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

### <span data-ttu-id="1ec81-169">-상태</span><span class="sxs-lookup"><span data-stu-id="1ec81-169">-State</span></span>
<span data-ttu-id="1ec81-170">지정 하는 경우 작업에 대 한 패키지가 선적 되었음을 가져오기/내보내기 서비스에 알려 주는 값을 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="1ec81-171">이 요청 또는 이전 요청에서 ReturnAddress 및 DeliveryPackage 속성이 설정 되어 있어야 하며 그렇지 않으면 요청이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="1ec81-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ec81-172">-SubscriptionId</span></span>
<span data-ttu-id="1ec81-173">Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="1ec81-174">태그</span><span class="sxs-lookup"><span data-stu-id="1ec81-174">-Tag</span></span>
<span data-ttu-id="1ec81-175">작업에 할당 되는 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="1ec81-176">-확인</span><span class="sxs-lookup"><span data-stu-id="1ec81-176">-Confirm</span></span>
<span data-ttu-id="1ec81-177">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec81-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec81-178">-WhatIf</span></span>
<span data-ttu-id="1ec81-179">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec81-180">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec81-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec81-181">CommonParameters</span></span>
<span data-ttu-id="1ec81-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec81-183">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ec81-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec81-184">입력</span><span class="sxs-lookup"><span data-stu-id="1ec81-184">INPUTS</span></span>

### <span data-ttu-id="1ec81-185">IImportExportIdentity 내보내기. i m a.</span><span class="sxs-lookup"><span data-stu-id="1ec81-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1ec81-186">출력</span><span class="sxs-lookup"><span data-stu-id="1ec81-186">OUTPUTS</span></span>

### <span data-ttu-id="1ec81-187">Api20161101 내보내기. i i a PowerShell. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="1ec81-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="1ec81-188">상속자</span><span class="sxs-lookup"><span data-stu-id="1ec81-188">NOTES</span></span>

<span data-ttu-id="1ec81-189">별칭과</span><span class="sxs-lookup"><span data-stu-id="1ec81-189">ALIASES</span></span>

<span data-ttu-id="1ec81-190">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1ec81-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ec81-191">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ec81-192">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ec81-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ec81-193">드라이브 목록 <IDriveStatus [] >: 작업을 구성 하는 드라이브 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="1ec81-194">`[BitLockerKey <String>]`: 드라이브를 암호화 하는 데 사용 되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="1ec81-195">`[BytesSucceeded <Int64?>]`: 드라이브에 대 한 바이트가 전송 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="1ec81-196">`[CopyStatus <String>]`: 데이터 전송 프로세스에 대 한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="1ec81-197">이 필드는 드라이브가 전송 상태에 있을 때까지 응답에 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="1ec81-198">`[DriveHeaderHash <String>]`: 드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="1ec81-199">`[DriveId <String>]`: 드라이브의 하드웨어 일련 번호 (공백 없음).</span><span class="sxs-lookup"><span data-stu-id="1ec81-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="1ec81-200">`[ErrorLogUri <String>]`: 데이터 전송 작업에 대 한 오류 로그를 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="1ec81-201">`[ManifestFile <String>]`: 드라이브의 매니페스트 파일에 대 한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="1ec81-202">`[ManifestHash <String>]`: 드라이브의 매니페스트 파일에 대 한 Base16 인코딩된 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="1ec81-203">`[ManifestUri <String>]`: 드라이브 매니페스트 파일을 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="1ec81-204">`[PercentComplete <Int32?>]`: 드라이브의 백분율이 완료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="1ec81-205">`[State <DriveState?>]`: 드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="1ec81-206">`[VerboseLogUri <String>]`: 데이터 전송 작업에 대 한 자세한 로그를 포함 하는 blob을 가리키는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="1ec81-207">INPUTOBJECT <IImportExportIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ec81-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ec81-208">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1ec81-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ec81-209">`[JobName <String>]`: 가져오기/내보내기 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1ec81-210">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1ec81-211">예를 들어 미국/동 또는 westus.</span><span class="sxs-lookup"><span data-stu-id="1ec81-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="1ec81-212">`[ResourceGroupName <String>]`: 리소스 그룹 이름은 사용자 구독 내에서 리소스 그룹을 고유 하 게 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1ec81-213">`[SubscriptionId <String>]`: Azure 사용자의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ec81-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1ec81-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ec81-214">RELATED LINKS</span></span>

