---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215587"
---
# <span data-ttu-id="7c80e-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c80e-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="7c80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c80e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c80e-103">컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-103">Gets a container registry.</span></span>

## <span data-ttu-id="7c80e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c80e-104">SYNTAX</span></span>

### <span data-ttu-id="7c80e-105">ListRegistriesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c80e-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c80e-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c80e-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c80e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c80e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c80e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c80e-108">DESCRIPTION</span></span>
<span data-ttu-id="7c80e-109">Get-AzContainerRegistry cmdlet은 지정 된 컨테이너 레지스트리 또는 리소스 그룹 또는 구독에 있는 모든 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="7c80e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c80e-110">EXAMPLES</span></span>

### <span data-ttu-id="7c80e-111">예제 1: 지정 된 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c80e-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7c80e-112">이 명령은 지정 된 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="7c80e-113">예제 2: 리소스 그룹의 모든 컨테이너 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c80e-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="7c80e-114">이 명령은 리소스 그룹의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="7c80e-115">예제 3: 구독에서 모든 컨테이너의 레지스트리 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c80e-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="7c80e-116">이 명령은 구독의 모든 컨테이너 레지스트리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="7c80e-117">변수</span><span class="sxs-lookup"><span data-stu-id="7c80e-117">PARAMETERS</span></span>

### <span data-ttu-id="7c80e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c80e-118">-DefaultProfile</span></span>
<span data-ttu-id="7c80e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c80e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c80e-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="7c80e-120">-IncludeDetail</span></span>
<span data-ttu-id="7c80e-121">컨테이너 레지스트리에 대 한 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="7c80e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7c80e-122">-Name</span></span>
<span data-ttu-id="7c80e-123">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="7c80e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c80e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c80e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c80e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c80e-126">-ResourceId</span></span>
<span data-ttu-id="7c80e-127">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="7c80e-127">The container registry resource id</span></span>

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

### <span data-ttu-id="7c80e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c80e-128">CommonParameters</span></span>
<span data-ttu-id="7c80e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c80e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c80e-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c80e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c80e-131">입력</span><span class="sxs-lookup"><span data-stu-id="7c80e-131">INPUTS</span></span>

### <span data-ttu-id="7c80e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c80e-132">System.String</span></span>

## <span data-ttu-id="7c80e-133">출력</span><span class="sxs-lookup"><span data-stu-id="7c80e-133">OUTPUTS</span></span>

### <span data-ttu-id="7c80e-134">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c80e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="7c80e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7c80e-135">NOTES</span></span>

## <span data-ttu-id="7c80e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c80e-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c80e-137">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c80e-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="7c80e-138">업데이트-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c80e-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="7c80e-139">제거-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c80e-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

