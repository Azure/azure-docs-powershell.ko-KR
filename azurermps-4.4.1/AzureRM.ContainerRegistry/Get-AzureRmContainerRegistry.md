---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531827"
---
# <span data-ttu-id="c57b2-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57b2-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="c57b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c57b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c57b2-103">컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c57b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c57b2-104">SYNTAX</span></span>

### <span data-ttu-id="c57b2-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57b2-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c57b2-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57b2-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c57b2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c57b2-107">DESCRIPTION</span></span>
<span data-ttu-id="c57b2-108">**AzureRmContainerRegistry** cmdlet은 지정 된 컨테이너 레지스트리 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너 레지스트리에 대해 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="c57b2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c57b2-109">EXAMPLES</span></span>

### <span data-ttu-id="c57b2-110">예제 1: 지정 된 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="c57b2-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="c57b2-111">이 명령은 지정 된 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="c57b2-112">예제 2: 리소스 그룹의 모든 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="c57b2-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="c57b2-113">이 명령은 리소스 그룹의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="c57b2-114">예제 3: 구독에서 모든 컨테이너의 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="c57b2-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="c57b2-115">이 명령은 구독의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="c57b2-116">변수</span><span class="sxs-lookup"><span data-stu-id="c57b2-116">PARAMETERS</span></span>

### <span data-ttu-id="c57b2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c57b2-117">-Name</span></span>
<span data-ttu-id="c57b2-118">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="c57b2-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57b2-121">-DefaultProfile</span></span>
<span data-ttu-id="c57b2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c57b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57b2-123">CommonParameters</span></span>
<span data-ttu-id="c57b2-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c57b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57b2-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57b2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57b2-126">입력</span><span class="sxs-lookup"><span data-stu-id="c57b2-126">INPUTS</span></span>

## <span data-ttu-id="c57b2-127">출력</span><span class="sxs-lookup"><span data-stu-id="c57b2-127">OUTPUTS</span></span>

### <span data-ttu-id="c57b2-128">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57b2-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c57b2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c57b2-129">NOTES</span></span>

## <span data-ttu-id="c57b2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c57b2-130">RELATED LINKS</span></span>

[<span data-ttu-id="c57b2-131">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57b2-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="c57b2-132">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57b2-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c57b2-133">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c57b2-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

