---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203076"
---
# <span data-ttu-id="e70a6-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e70a6-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="e70a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e70a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e70a6-103">서비스 태그 정보 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="e70a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="e70a6-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e70a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="e70a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e70a6-106">**Get-AzNetworkServiceTag** cmdlet은 서비스 태그 정보 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="e70a6-107">지정한 Azure 지역 정보는 위치에 따라 필터가 아닌 버전에 대한 참조로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="e70a6-108">예를 들어 지정한 경우에도 구독이 속한 클라우드(예: 공용, 미국 정부, 중국 또는 독일)로 제한되는 모든 지역에서는 전체에 대한 세부 정보가 있는 서비스 태그 목록을 얻게 `-Location eastus2` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="e70a6-109">예제</span><span class="sxs-lookup"><span data-stu-id="e70a6-109">EXAMPLES</span></span>

### <span data-ttu-id="e70a6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e70a6-110">Example 1</span></span>
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

<span data-ttu-id="e70a6-111">이 명령은 서비스 태그 정보 리소스 목록을 사용하여 변수에 `serviceTags` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="e70a6-112">예제 2: AzureSQL에 대한 모든 주소 연결점 얻기</span><span class="sxs-lookup"><span data-stu-id="e70a6-112">Example 2: Get all address prefixes for AzureSQL</span></span>
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

<span data-ttu-id="e70a6-113">첫 번째 명령은 서비스 태그 정보 리소스 목록을 사용하여 변수에 `serviceTags` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="e70a6-114">두 번째 명령은 목록을 필터하여 Sql에 대한 정보 리소스를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="e70a6-115">예제 3: 미국 서부 2에 대한 Storage의 서비스 태그 정보 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="e70a6-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
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

<span data-ttu-id="e70a6-116">첫 번째 명령은 서비스 태그 정보 리소스 목록을 사용하여 변수에 `serviceTags` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="e70a6-117">다음 명령은 목록을 필터링하여 미국 서부 2의 Storage에 대한 서비스 태그 정보를 선택하는 다양한 방법을 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="e70a6-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="e70a6-118">예제 4: 모든 전역 서비스 태그 정보 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="e70a6-118">Example 4: Get all global service tag information resources</span></span>
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

<span data-ttu-id="e70a6-119">첫 번째 명령은 서비스 태그 정보 리소스 목록을 사용하여 변수에 `serviceTags` 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="e70a6-120">두 번째 명령은 지역을 설정하지 않은 항목만 선택하기 위해 목록을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="e70a6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e70a6-121">PARAMETERS</span></span>

### <span data-ttu-id="e70a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70a6-122">-DefaultProfile</span></span>
<span data-ttu-id="e70a6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e70a6-124">-Location</span><span class="sxs-lookup"><span data-stu-id="e70a6-124">-Location</span></span>
<span data-ttu-id="e70a6-125">버전에 대한 참조로 사용될 위치(위치를 기준으로 필터가 아닌, 모든 지역에 걸쳐, 구독이 속한 클라우드로 제한되는 서비스 태그 목록을 얻게 되지만)</span><span class="sxs-lookup"><span data-stu-id="e70a6-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

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

### <span data-ttu-id="e70a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70a6-126">CommonParameters</span></span>
<span data-ttu-id="e70a6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e70a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70a6-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e70a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70a6-129">입력</span><span class="sxs-lookup"><span data-stu-id="e70a6-129">INPUTS</span></span>

### <span data-ttu-id="e70a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e70a6-130">System.String</span></span>

## <span data-ttu-id="e70a6-131">출력</span><span class="sxs-lookup"><span data-stu-id="e70a6-131">OUTPUTS</span></span>

### <span data-ttu-id="e70a6-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e70a6-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="e70a6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e70a6-133">NOTES</span></span>

## <span data-ttu-id="e70a6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e70a6-134">RELATED LINKS</span></span>
