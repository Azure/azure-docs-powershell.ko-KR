---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: f833d2f46c67964356f48a06c35d41dfcf090fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697135"
---
# <span data-ttu-id="2d54f-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d54f-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="2d54f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d54f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d54f-103">컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-103">Gets a container registry.</span></span>

## <span data-ttu-id="2d54f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d54f-104">SYNTAX</span></span>

### <span data-ttu-id="2d54f-105">ListRegistriesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d54f-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d54f-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d54f-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d54f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d54f-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d54f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2d54f-108">DESCRIPTION</span></span>
<span data-ttu-id="2d54f-109">Get-AzContainerRegistry cmdlet은 지정 된 컨테이너 레지스트리 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="2d54f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2d54f-110">EXAMPLES</span></span>

### <span data-ttu-id="2d54f-111">예제 1: 지정 된 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d54f-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="2d54f-112">이 명령은 지정 된 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="2d54f-113">예제 2: 리소스 그룹의 모든 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d54f-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="2d54f-114">이 명령은 리소스 그룹의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="2d54f-115">예제 3: 구독에서 모든 컨테이너의 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="2d54f-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

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

<span data-ttu-id="2d54f-116">이 명령은 구독의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="2d54f-117">변수</span><span class="sxs-lookup"><span data-stu-id="2d54f-117">PARAMETERS</span></span>

### <span data-ttu-id="2d54f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d54f-118">-DefaultProfile</span></span>
<span data-ttu-id="2d54f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2d54f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d54f-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="2d54f-120">-IncludeDetail</span></span>
<span data-ttu-id="2d54f-121">컨테이너 레지스트리에 대 한 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="2d54f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="2d54f-122">-Name</span></span>
<span data-ttu-id="2d54f-123">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="2d54f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d54f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d54f-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2d54f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d54f-126">-ResourceId</span></span>
<span data-ttu-id="2d54f-127">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2d54f-127">The container registry resource id</span></span>

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

### <span data-ttu-id="2d54f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d54f-128">CommonParameters</span></span>
<span data-ttu-id="2d54f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d54f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d54f-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d54f-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d54f-131">입력</span><span class="sxs-lookup"><span data-stu-id="2d54f-131">INPUTS</span></span>

### <span data-ttu-id="2d54f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d54f-132">System.String</span></span>

## <span data-ttu-id="2d54f-133">출력</span><span class="sxs-lookup"><span data-stu-id="2d54f-133">OUTPUTS</span></span>

### <span data-ttu-id="2d54f-134">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d54f-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="2d54f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2d54f-135">NOTES</span></span>

## <span data-ttu-id="2d54f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d54f-136">RELATED LINKS</span></span>

[<span data-ttu-id="2d54f-137">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d54f-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="2d54f-138">업데이트-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d54f-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="2d54f-139">제거-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d54f-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

