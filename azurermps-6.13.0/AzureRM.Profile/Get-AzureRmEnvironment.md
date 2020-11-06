---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530137"
---
# <span data-ttu-id="876a5-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="876a5-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="876a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876a5-102">SYNOPSIS</span></span>
<span data-ttu-id="876a5-103">Azure services 인스턴스에 대 한 끝점 및 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="876a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="876a5-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876a5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="876a5-105">DESCRIPTION</span></span>
<span data-ttu-id="876a5-106">Get-AzureRmEnvironment cmdlet은 Azure services 인스턴스에 대 한 끝점 및 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="876a5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="876a5-107">EXAMPLES</span></span>

### <span data-ttu-id="876a5-108">예제 1: AzureCloud 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="876a5-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="876a5-109">이 예제에서는 AzureCloud (기본) 환경에 대 한 끝점 및 메타 데이터를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="876a5-110">예제 2: AzureChinaCloud 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="876a5-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="876a5-111">이 예제에서는 AzureChinaCloud 환경에 대 한 끝점 및 메타 데이터를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="876a5-112">예제 3: AzureUSGovernment 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="876a5-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="876a5-113">이 예제에서는 AzureUSGovernment 환경에 대 한 끝점 및 메타 데이터를 가져오는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="876a5-114">변수</span><span class="sxs-lookup"><span data-stu-id="876a5-114">PARAMETERS</span></span>

### <span data-ttu-id="876a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876a5-115">-DefaultProfile</span></span>
<span data-ttu-id="876a5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876a5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="876a5-117">-Name</span></span>
<span data-ttu-id="876a5-118">가져올 Azure 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876a5-119">CommonParameters</span></span>
<span data-ttu-id="876a5-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="876a5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876a5-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876a5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876a5-122">입력</span><span class="sxs-lookup"><span data-stu-id="876a5-122">INPUTS</span></span>

### <span data-ttu-id="876a5-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="876a5-123">System.String</span></span>

## <span data-ttu-id="876a5-124">출력</span><span class="sxs-lookup"><span data-stu-id="876a5-124">OUTPUTS</span></span>

### <span data-ttu-id="876a5-125">Microsoft. Azure. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="876a5-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="876a5-126">상속자</span><span class="sxs-lookup"><span data-stu-id="876a5-126">NOTES</span></span>

## <span data-ttu-id="876a5-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="876a5-127">RELATED LINKS</span></span>

[<span data-ttu-id="876a5-128">추가-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="876a5-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="876a5-129">제거-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="876a5-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="876a5-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="876a5-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

