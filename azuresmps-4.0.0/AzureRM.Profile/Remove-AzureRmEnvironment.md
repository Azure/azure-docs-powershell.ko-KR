---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701750"
---
# <span data-ttu-id="e2e38-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2e38-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="e2e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e38-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e38-103">지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="e2e38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2e38-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2e38-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e38-106">Remove-AzureRmEnvironment cmdlet은 지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="e2e38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2e38-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e38-108">예제 1: 테스트 환경 만들기 및 제거</span><span class="sxs-lookup"><span data-stu-id="e2e38-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="e2e38-109">이 예제에서는 AzureRmEnvironment를 사용 하 여 환경을 만드는 방법과 Remove-AzureRmEnvironment를 사용 하 여 환경을 삭제 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="e2e38-110">변수</span><span class="sxs-lookup"><span data-stu-id="e2e38-110">PARAMETERS</span></span>

### <span data-ttu-id="e2e38-111">-이름</span><span class="sxs-lookup"><span data-stu-id="e2e38-111">-Name</span></span>
<span data-ttu-id="e2e38-112">제거할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e38-113">-확인</span><span class="sxs-lookup"><span data-stu-id="e2e38-113">-Confirm</span></span>
<span data-ttu-id="e2e38-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e38-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e38-115">-WhatIf</span></span>
<span data-ttu-id="e2e38-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e38-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e38-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e38-118">CommonParameters</span></span>
<span data-ttu-id="e2e38-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e38-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e38-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e38-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e38-121">입력</span><span class="sxs-lookup"><span data-stu-id="e2e38-121">INPUTS</span></span>

## <span data-ttu-id="e2e38-122">출력</span><span class="sxs-lookup"><span data-stu-id="e2e38-122">OUTPUTS</span></span>

### <span data-ttu-id="e2e38-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2e38-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="e2e38-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e2e38-124">NOTES</span></span>

## <span data-ttu-id="e2e38-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2e38-125">RELATED LINKS</span></span>

[<span data-ttu-id="e2e38-126">추가-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2e38-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="e2e38-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2e38-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="e2e38-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2e38-128">Set-AzureRMEnvironment</span></span>]()

