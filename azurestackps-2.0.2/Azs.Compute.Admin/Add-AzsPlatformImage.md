---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046910"
---
# <span data-ttu-id="975a5-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="975a5-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="975a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="975a5-102">SYNOPSIS</span></span>
<span data-ttu-id="975a5-103">지정 된 게시자, 제공, sku 및 버전이 있는 새 플랫폼 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="975a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="975a5-104">SYNTAX</span></span>

### <span data-ttu-id="975a5-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="975a5-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="975a5-106">만드는</span><span class="sxs-lookup"><span data-stu-id="975a5-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="975a5-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="975a5-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="975a5-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="975a5-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="975a5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="975a5-109">DESCRIPTION</span></span>
<span data-ttu-id="975a5-110">지정 된 게시자, 제공, sku 및 버전이 있는 새 플랫폼 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="975a5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="975a5-111">EXAMPLES</span></span>

### <span data-ttu-id="975a5-112">예제 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="975a5-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="975a5-113">Blob Storage에서 플랫폼 이미지를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="975a5-114">A SasUri를 사용 하 여 PlatformImage의 위치를 지정 하거나 공개적으로 액세스할 수 있는 URL을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="975a5-115">변수</span><span class="sxs-lookup"><span data-stu-id="975a5-115">PARAMETERS</span></span>

### <span data-ttu-id="975a5-116">예외. 메시지</span><span class="sxs-lookup"><span data-stu-id="975a5-116">Exception.Message</span></span>
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

### <span data-ttu-id="975a5-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="975a5-117">-BillingPartNumber</span></span>
<span data-ttu-id="975a5-118">부품 번호는 소프트웨어 비용을 청구 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-119">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="975a5-119">-DataDisks</span></span>
<span data-ttu-id="975a5-120">플랫폼 이미지에 사용 되는 데이터 디스크</span><span class="sxs-lookup"><span data-stu-id="975a5-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="975a5-121">생성 하려면 DATADISKS 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975a5-122">-DefaultProfile</span></span>
<span data-ttu-id="975a5-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975a5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="975a5-124">-InputObject</span></span>
<span data-ttu-id="975a5-125">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-126">-위치</span><span class="sxs-lookup"><span data-stu-id="975a5-126">-Location</span></span>
<span data-ttu-id="975a5-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="975a5-128">-NewImage</span></span>
<span data-ttu-id="975a5-129">새 플랫폼 이미지를 만드는 데 사용 되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="975a5-130">생성 하려면 NEWIMAGE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="975a5-131">-NoWait</span></span>
<span data-ttu-id="975a5-132">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="975a5-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="975a5-133">-제공</span><span class="sxs-lookup"><span data-stu-id="975a5-133">-Offer</span></span>
<span data-ttu-id="975a5-134">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="975a5-135">-OsType</span></span>
<span data-ttu-id="975a5-136">운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="975a5-137">-OsUri</span></span>
<span data-ttu-id="975a5-138">디스크의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="975a5-139">-ProvisioningState</span></span>
<span data-ttu-id="975a5-140">플랫폼 이미지의 프로 비전 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="975a5-141">-Publisher</span></span>
<span data-ttu-id="975a5-142">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="975a5-143">-Sku</span></span>
<span data-ttu-id="975a5-144">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="975a5-145">-SubscriptionId</span></span>
<span data-ttu-id="975a5-146">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="975a5-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-148">-버전</span><span class="sxs-lookup"><span data-stu-id="975a5-148">-Version</span></span>
<span data-ttu-id="975a5-149">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="975a5-150">-확인</span><span class="sxs-lookup"><span data-stu-id="975a5-150">-Confirm</span></span>
<span data-ttu-id="975a5-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="975a5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975a5-152">-WhatIf</span></span>
<span data-ttu-id="975a5-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="975a5-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="975a5-155">예외. 메시지</span><span class="sxs-lookup"><span data-stu-id="975a5-155">Exception.Message</span></span>

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

### <span data-ttu-id="975a5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975a5-156">CommonParameters</span></span>
<span data-ttu-id="975a5-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975a5-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="975a5-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975a5-159">입력</span><span class="sxs-lookup"><span data-stu-id="975a5-159">INPUTS</span></span>

### <span data-ttu-id="975a5-160">Api20151201Preview. t t t. t t t. t t t t-t Platformimage매개 변수</span><span class="sxs-lookup"><span data-stu-id="975a5-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="975a5-161">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="975a5-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="975a5-162">출력</span><span class="sxs-lookup"><span data-stu-id="975a5-162">OUTPUTS</span></span>

### <span data-ttu-id="975a5-163">Api20151201Preview. t t t. t t t.</span><span class="sxs-lookup"><span data-stu-id="975a5-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="975a5-164">상속자</span><span class="sxs-lookup"><span data-stu-id="975a5-164">NOTES</span></span>

<span data-ttu-id="975a5-165">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="975a5-166">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="975a5-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="975a5-167">DATADISKS <IDataDisk [] >: 플랫폼 이미지에 사용 되는 데이터 디스크입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="975a5-168">`[Lun <Int32?>]`: 논리 단위 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="975a5-169">`[Uri <String>]`: 디스크 템플릿의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="975a5-170">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="975a5-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="975a5-171">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="975a5-172">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="975a5-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="975a5-173">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="975a5-174">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="975a5-175">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="975a5-176">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="975a5-177">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="975a5-178">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="975a5-179">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="975a5-180">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="975a5-181">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="975a5-182">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="975a5-183">NEWIMAGE <IPlatformImageParameters> : 새 플랫폼 이미지를 만드는 데 사용 되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="975a5-184">`[DataDisk <IDataDisk[]>]`: 플랫폼 이미지에 사용 되는 데이터 디스크입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="975a5-185">`[Lun <Int32?>]`: 논리 단위 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="975a5-186">`[Uri <String>]`: 디스크 템플릿의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="975a5-187">`[DetailBillingPartNumber <String>]`: 부품 번호는 소프트웨어 비용을 청구 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="975a5-188">`[OSDiskOstype <OSType?>]`: 운영 체제 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="975a5-189">`[OSDiskUri <String>]`: 디스크의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="975a5-190">`[ProvisioningState <ProvisioningState?>]`: 플랫폼 이미지의 프로 비전 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="975a5-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="975a5-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="975a5-191">RELATED LINKS</span></span>

