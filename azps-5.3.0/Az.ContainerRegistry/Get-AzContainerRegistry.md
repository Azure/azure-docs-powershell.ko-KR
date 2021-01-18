---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493763"
---
# <span data-ttu-id="a85d3-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85d3-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="a85d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a85d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a85d3-103">컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-103">Gets a container registry.</span></span>

## <span data-ttu-id="a85d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="a85d3-104">SYNTAX</span></span>

### <span data-ttu-id="a85d3-105">ListRegistriesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a85d3-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85d3-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a85d3-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a85d3-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a85d3-108">설명</span><span class="sxs-lookup"><span data-stu-id="a85d3-108">DESCRIPTION</span></span>
<span data-ttu-id="a85d3-109">Get-AzContainerRegistry cmdlet은 지정된 컨테이너 레지스트리 또는 리소스 그룹 또는 구독의 모든 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="a85d3-110">예제</span><span class="sxs-lookup"><span data-stu-id="a85d3-110">EXAMPLES</span></span>

### <span data-ttu-id="a85d3-111">예제 1: 지정된 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="a85d3-112">이 명령은 지정된 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="a85d3-113">예제 2: 리소스 그룹의 모든 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="a85d3-114">이 명령은 리소스 그룹의 모든 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="a85d3-115">예제 3: 구독의 모든 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="a85d3-116">이 명령은 구독의 모든 컨테이너 레지스트리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="a85d3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a85d3-117">PARAMETERS</span></span>

### <span data-ttu-id="a85d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85d3-118">-DefaultProfile</span></span>
<span data-ttu-id="a85d3-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a85d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a85d3-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a85d3-120">-IncludeDetail</span></span>
<span data-ttu-id="a85d3-121">컨테이너 레지스트리에 대한 자세한 내용을 보여 웁니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="a85d3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a85d3-122">-Name</span></span>
<span data-ttu-id="a85d3-123">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="a85d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="a85d3-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a85d3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a85d3-126">-ResourceId</span></span>
<span data-ttu-id="a85d3-127">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a85d3-127">The container registry resource id</span></span>

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

### <span data-ttu-id="a85d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85d3-128">CommonParameters</span></span>
<span data-ttu-id="a85d3-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a85d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85d3-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a85d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85d3-131">입력</span><span class="sxs-lookup"><span data-stu-id="a85d3-131">INPUTS</span></span>

### <span data-ttu-id="a85d3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a85d3-132">System.String</span></span>

## <span data-ttu-id="a85d3-133">출력</span><span class="sxs-lookup"><span data-stu-id="a85d3-133">OUTPUTS</span></span>

### <span data-ttu-id="a85d3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85d3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="a85d3-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a85d3-135">NOTES</span></span>

## <span data-ttu-id="a85d3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a85d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="a85d3-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85d3-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="a85d3-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85d3-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="a85d3-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a85d3-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

