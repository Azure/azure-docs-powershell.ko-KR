---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048921"
---
# <span data-ttu-id="375ef-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="375ef-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="375ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="375ef-102">SYNOPSIS</span></span>
<span data-ttu-id="375ef-103">서비스 태그 정보 리소스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="375ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="375ef-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="375ef-105">DESCRIPTION</span></span>
<span data-ttu-id="375ef-106">**Get-AzNetworkServiceTag** cmdlet은 서비스 태그 정보 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="375ef-107">지정 하는 Azure 지역 정보는 위치를 기반으로 하는 필터가 아니라 버전에 대 한 참조로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="375ef-108">예를 들어 사용자가 지정 하는 경우에도 `-Location eastus2` 모든 지역에서 접두사 세부 정보를 사용 하 여 서비스 태그 목록을 가져오고 구독이 속해 있는 클라우드로 제한 (예: 공개, 미국 정부, 중국 또는 독일) 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="375ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="375ef-109">EXAMPLES</span></span>

### <span data-ttu-id="375ef-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="375ef-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="375ef-111">명령에서 서비스 태그 정보 리소스 목록을 가져와 변수에 저장 `serviceTags` 합니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="375ef-112">예제 2: AzureSQL의 모든 주소 접두사 가져오기</span><span class="sxs-lookup"><span data-stu-id="375ef-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="375ef-113">첫 번째 명령은 서비스 태그 정보 리소스 목록을 가져와 변수에 저장 합니다 `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="375ef-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="375ef-114">두 번째 명령은 목록에서 Sql에 대 한 정보 리소스를 선택 하도록 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="375ef-115">예제 3: 미국 2에 대 한 저장소 서비스 태그 정보 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="375ef-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="375ef-116">첫 번째 명령은 서비스 태그 정보 리소스 목록을 가져와 변수에 저장 합니다 `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="375ef-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="375ef-117">다음 명령은 US 2에서 저장소에 대 한 서비스 태그 정보를 선택 하도록 목록을 필터링 하는 다양 한 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="375ef-118">예제 4: 모든 글로벌 서비스 태그 정보 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="375ef-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="375ef-119">첫 번째 명령은 서비스 태그 정보 리소스 목록을 가져와 변수에 저장 합니다 `serviceTags` .</span><span class="sxs-lookup"><span data-stu-id="375ef-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="375ef-120">두 번째 명령은 목록에서 set region이 없는 필드만 선택 하도록 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="375ef-121">변수</span><span class="sxs-lookup"><span data-stu-id="375ef-121">PARAMETERS</span></span>

### <span data-ttu-id="375ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375ef-122">-DefaultProfile</span></span>
<span data-ttu-id="375ef-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="375ef-124">-위치</span><span class="sxs-lookup"><span data-stu-id="375ef-124">-Location</span></span>
<span data-ttu-id="375ef-125">위치를 기반으로 하는 필터가 아니라 버전에 대 한 참조로 사용할 위치 이며, 모든 지역에서 접두사 세부 정보를 사용 하 여 서비스 태그 목록을 가져올 수 있지만 구독이 속해 있는 클라우드로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="375ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375ef-126">CommonParameters</span></span>
<span data-ttu-id="375ef-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="375ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375ef-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="375ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375ef-129">입력</span><span class="sxs-lookup"><span data-stu-id="375ef-129">INPUTS</span></span>

### <span data-ttu-id="375ef-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="375ef-130">System.String</span></span>

## <span data-ttu-id="375ef-131">출력</span><span class="sxs-lookup"><span data-stu-id="375ef-131">OUTPUTS</span></span>

### <span data-ttu-id="375ef-132">Microsoft. 네트워크 모델. PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="375ef-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="375ef-133">상속자</span><span class="sxs-lookup"><span data-stu-id="375ef-133">NOTES</span></span>

## <span data-ttu-id="375ef-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="375ef-134">RELATED LINKS</span></span>
