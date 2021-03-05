---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: b3bccc5d538c8ce5e3a79b621b48d75556ed0189
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981339"
---
# <span data-ttu-id="56f27-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="56f27-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="56f27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f27-102">SYNOPSIS</span></span>
<span data-ttu-id="56f27-103">Azure 서비스의 인스턴스에 대한 엔드포인트 및 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="56f27-104">구문</span><span class="sxs-lookup"><span data-stu-id="56f27-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f27-105">설명</span><span class="sxs-lookup"><span data-stu-id="56f27-105">DESCRIPTION</span></span>
<span data-ttu-id="56f27-106">Get-AzEnvironment cmdlet은 Azure 서비스의 인스턴스에 대한 엔드포인트 및 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="56f27-107">예제</span><span class="sxs-lookup"><span data-stu-id="56f27-107">EXAMPLES</span></span>

### <span data-ttu-id="56f27-108">예제 1: AzureCloud 환경 사용</span><span class="sxs-lookup"><span data-stu-id="56f27-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="56f27-109">이 예제에서는 AzureCloud(기본값) 환경에 대한 엔드포인트 및 메타데이터를 얻을 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="56f27-110">예제 2: AzureChinaCloud 환경 사용</span><span class="sxs-lookup"><span data-stu-id="56f27-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="56f27-111">이 예제에서는 AzureChinaCloud 환경에 대한 엔드포인트 및 메타데이터를 얻을 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="56f27-112">예제 3: AzureUSGovernment 환경 사용</span><span class="sxs-lookup"><span data-stu-id="56f27-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="56f27-113">이 예제에서는 AzureUSGovernment 환경에 대한 엔드포인트 및 메타데이터를 얻을 수 있는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="56f27-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56f27-114">PARAMETERS</span></span>

### <span data-ttu-id="56f27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f27-115">-DefaultProfile</span></span>
<span data-ttu-id="56f27-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="56f27-117">-Name</span></span>
<span data-ttu-id="56f27-118">얻을 Azure 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="56f27-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f27-119">CommonParameters</span></span>
<span data-ttu-id="56f27-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56f27-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f27-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56f27-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f27-122">입력</span><span class="sxs-lookup"><span data-stu-id="56f27-122">INPUTS</span></span>

### <span data-ttu-id="56f27-123">System.String</span><span class="sxs-lookup"><span data-stu-id="56f27-123">System.String</span></span>

## <span data-ttu-id="56f27-124">출력</span><span class="sxs-lookup"><span data-stu-id="56f27-124">OUTPUTS</span></span>

### <span data-ttu-id="56f27-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="56f27-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="56f27-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56f27-126">NOTES</span></span>

## <span data-ttu-id="56f27-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56f27-127">RELATED LINKS</span></span>

[<span data-ttu-id="56f27-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="56f27-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="56f27-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="56f27-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="56f27-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="56f27-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

