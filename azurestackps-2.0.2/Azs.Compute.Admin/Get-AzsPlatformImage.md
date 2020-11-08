---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046744"
---
# <span data-ttu-id="59d99-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="59d99-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="59d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d99-102">SYNOPSIS</span></span>
<span data-ttu-id="59d99-103">게시자, 제안, sku 및 버전과 일치 하는 특정 플랫폼 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="59d99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59d99-104">SYNTAX</span></span>

### <span data-ttu-id="59d99-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="59d99-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="59d99-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="59d99-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59d99-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="59d99-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="59d99-108">설명은</span><span class="sxs-lookup"><span data-stu-id="59d99-108">DESCRIPTION</span></span>
<span data-ttu-id="59d99-109">게시자, 제안, sku 및 버전과 일치 하는 특정 플랫폼 이미지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="59d99-110">예제의</span><span class="sxs-lookup"><span data-stu-id="59d99-110">EXAMPLES</span></span>

### <span data-ttu-id="59d99-111">예제 1: 모든 플랫폼 이미지 가져오기</span><span class="sxs-lookup"><span data-stu-id="59d99-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="59d99-112">모든 매개 변수를 비워 두어 모든 플랫폼 이미지의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="59d99-113">예제 2: 특정 플랫폼 이미지 가져오기</span><span class="sxs-lookup"><span data-stu-id="59d99-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="59d99-114">플랫폼 이미지를 검색할 제공, 게시자, 위치, Sku 및 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="59d99-115">변수</span><span class="sxs-lookup"><span data-stu-id="59d99-115">PARAMETERS</span></span>

### <span data-ttu-id="59d99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d99-116">-DefaultProfile</span></span>
<span data-ttu-id="59d99-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d99-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59d99-118">-InputObject</span></span>
<span data-ttu-id="59d99-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-120">-위치</span><span class="sxs-lookup"><span data-stu-id="59d99-120">-Location</span></span>
<span data-ttu-id="59d99-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-122">-제공</span><span class="sxs-lookup"><span data-stu-id="59d99-122">-Offer</span></span>
<span data-ttu-id="59d99-123">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-123">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="59d99-124">-Publisher</span></span>
<span data-ttu-id="59d99-125">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-125">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="59d99-126">-Sku</span></span>
<span data-ttu-id="59d99-127">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-127">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59d99-128">-SubscriptionId</span></span>
<span data-ttu-id="59d99-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59d99-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-131">-버전</span><span class="sxs-lookup"><span data-stu-id="59d99-131">-Version</span></span>
<span data-ttu-id="59d99-132">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-132">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59d99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d99-133">CommonParameters</span></span>
<span data-ttu-id="59d99-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d99-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59d99-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d99-136">입력</span><span class="sxs-lookup"><span data-stu-id="59d99-136">INPUTS</span></span>

### <span data-ttu-id="59d99-137">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="59d99-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="59d99-138">출력</span><span class="sxs-lookup"><span data-stu-id="59d99-138">OUTPUTS</span></span>

### <span data-ttu-id="59d99-139">Api20151201Preview. t t t. t t t.</span><span class="sxs-lookup"><span data-stu-id="59d99-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="59d99-140">상속자</span><span class="sxs-lookup"><span data-stu-id="59d99-140">NOTES</span></span>

<span data-ttu-id="59d99-141">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59d99-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="59d99-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="59d99-143">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="59d99-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59d99-144">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="59d99-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="59d99-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59d99-146">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="59d99-147">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="59d99-148">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="59d99-149">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="59d99-150">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="59d99-151">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="59d99-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="59d99-153">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="59d99-154">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="59d99-155">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="59d99-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="59d99-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59d99-156">RELATED LINKS</span></span>

