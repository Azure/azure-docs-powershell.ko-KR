---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524516"
---
# <span data-ttu-id="43819-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43819-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="43819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43819-102">SYNOPSIS</span></span>
<span data-ttu-id="43819-103">컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43819-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43819-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43819-104">SYNTAX</span></span>

### <span data-ttu-id="43819-105">ListRegistriesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="43819-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43819-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43819-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43819-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43819-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43819-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43819-108">DESCRIPTION</span></span>
<span data-ttu-id="43819-109">Get-AzureRmContainerRegistry cmdlet은 지정 된 컨테이너 레지스트리 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43819-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="43819-110">예제의</span><span class="sxs-lookup"><span data-stu-id="43819-110">EXAMPLES</span></span>

### <span data-ttu-id="43819-111">예제 1: 지정 된 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="43819-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="43819-112">이 명령은 지정 된 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43819-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="43819-113">예제 2: 리소스 그룹의 모든 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="43819-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="43819-114">이 명령은 리소스 그룹의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43819-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="43819-115">예제 3: 구독에서 모든 컨테이너의 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="43819-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="43819-116">이 명령은 구독의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43819-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="43819-117">변수</span><span class="sxs-lookup"><span data-stu-id="43819-117">PARAMETERS</span></span>

### <span data-ttu-id="43819-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43819-118">-DefaultProfile</span></span>
<span data-ttu-id="43819-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43819-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43819-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="43819-120">-IncludeDetail</span></span>
<span data-ttu-id="43819-121">컨테이너 레지스트리에 대 한 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43819-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="43819-122">-이름</span><span class="sxs-lookup"><span data-stu-id="43819-122">-Name</span></span>
<span data-ttu-id="43819-123">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43819-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="43819-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43819-124">-ResourceGroupName</span></span>
<span data-ttu-id="43819-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43819-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
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

### <span data-ttu-id="43819-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43819-126">-ResourceId</span></span>
<span data-ttu-id="43819-127">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="43819-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43819-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43819-128">CommonParameters</span></span>
<span data-ttu-id="43819-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43819-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43819-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43819-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43819-131">입력</span><span class="sxs-lookup"><span data-stu-id="43819-131">INPUTS</span></span>

### <span data-ttu-id="43819-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43819-132">System.String</span></span>

## <span data-ttu-id="43819-133">출력</span><span class="sxs-lookup"><span data-stu-id="43819-133">OUTPUTS</span></span>

### <span data-ttu-id="43819-134">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43819-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="43819-135">상속자</span><span class="sxs-lookup"><span data-stu-id="43819-135">NOTES</span></span>

## <span data-ttu-id="43819-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43819-136">RELATED LINKS</span></span>

[<span data-ttu-id="43819-137">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43819-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="43819-138">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43819-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="43819-139">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="43819-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

