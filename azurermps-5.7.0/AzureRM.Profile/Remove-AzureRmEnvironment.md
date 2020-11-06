---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534759"
---
# <span data-ttu-id="41f26-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="41f26-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="41f26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f26-102">SYNOPSIS</span></span>
<span data-ttu-id="41f26-103">지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41f26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41f26-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41f26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41f26-105">DESCRIPTION</span></span>
<span data-ttu-id="41f26-106">Remove-AzureRmEnvironment cmdlet은 지정 된 Azure 인스턴스에 연결 하기 위한 끝점 및 메타 데이터 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="41f26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41f26-107">EXAMPLES</span></span>

### <span data-ttu-id="41f26-108">예제 1: 테스트 환경 만들기 및 제거</span><span class="sxs-lookup"><span data-stu-id="41f26-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="41f26-109">이 예제에서는 AzureRmEnvironment를 사용 하 여 환경을 만드는 방법과 Remove-AzureRmEnvironment를 사용 하 여 환경을 삭제 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="41f26-110">변수</span><span class="sxs-lookup"><span data-stu-id="41f26-110">PARAMETERS</span></span>

### <span data-ttu-id="41f26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f26-111">-DefaultProfile</span></span>
<span data-ttu-id="41f26-112">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f26-113">-이름</span><span class="sxs-lookup"><span data-stu-id="41f26-113">-Name</span></span>
<span data-ttu-id="41f26-114">제거할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="41f26-115">-범위</span><span class="sxs-lookup"><span data-stu-id="41f26-115">-Scope</span></span>
<span data-ttu-id="41f26-116">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f26-117">-확인</span><span class="sxs-lookup"><span data-stu-id="41f26-117">-Confirm</span></span>
<span data-ttu-id="41f26-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41f26-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41f26-119">-WhatIf</span></span>
<span data-ttu-id="41f26-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41f26-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41f26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f26-122">CommonParameters</span></span>
<span data-ttu-id="41f26-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f26-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f26-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f26-125">입력</span><span class="sxs-lookup"><span data-stu-id="41f26-125">INPUTS</span></span>

### <span data-ttu-id="41f26-126">않아야</span><span class="sxs-lookup"><span data-stu-id="41f26-126">None</span></span>
<span data-ttu-id="41f26-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41f26-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41f26-128">출력</span><span class="sxs-lookup"><span data-stu-id="41f26-128">OUTPUTS</span></span>

### <span data-ttu-id="41f26-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="41f26-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="41f26-130">상속자</span><span class="sxs-lookup"><span data-stu-id="41f26-130">NOTES</span></span>

## <span data-ttu-id="41f26-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41f26-131">RELATED LINKS</span></span>

[<span data-ttu-id="41f26-132">추가-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="41f26-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="41f26-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="41f26-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="41f26-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="41f26-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

