---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703875"
---
# <span data-ttu-id="8f921-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8f921-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="8f921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f921-102">SYNOPSIS</span></span>
<span data-ttu-id="8f921-103">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f921-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f921-104">SYNTAX</span></span>

### <span data-ttu-id="8f921-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f921-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f921-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f921-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f921-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f921-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f921-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f921-108">DESCRIPTION</span></span>
<span data-ttu-id="8f921-109">Remove-AzureRmContainerRegistryReplication cmdlet은 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="8f921-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8f921-110">EXAMPLES</span></span>

### <span data-ttu-id="8f921-111">예제 1: 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="8f921-112">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="8f921-113">변수</span><span class="sxs-lookup"><span data-stu-id="8f921-113">PARAMETERS</span></span>

### <span data-ttu-id="8f921-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f921-114">-DefaultProfile</span></span>
<span data-ttu-id="8f921-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f921-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8f921-116">-Name</span></span>
<span data-ttu-id="8f921-117">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="8f921-118">위치 이름을 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f921-119">-PassThru</span></span>
<span data-ttu-id="8f921-120">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="8f921-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8f921-121">-RegistryName</span></span>
<span data-ttu-id="8f921-122">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="8f921-123">-Replicatoin</span></span>
<span data-ttu-id="8f921-124">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f921-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f921-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f921-127">-ResourceId</span></span>
<span data-ttu-id="8f921-128">컨테이너 레지스트리 복제 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8f921-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="8f921-129">-확인</span><span class="sxs-lookup"><span data-stu-id="8f921-129">-Confirm</span></span>
<span data-ttu-id="8f921-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f921-131">-WhatIf</span></span>
<span data-ttu-id="8f921-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f921-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f921-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f921-134">CommonParameters</span></span>
<span data-ttu-id="8f921-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f921-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f921-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f921-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f921-137">입력</span><span class="sxs-lookup"><span data-stu-id="8f921-137">INPUTS</span></span>

### <span data-ttu-id="8f921-138">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8f921-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="8f921-139">매개 변수: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f921-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="8f921-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f921-140">System.String</span></span>

## <span data-ttu-id="8f921-141">출력</span><span class="sxs-lookup"><span data-stu-id="8f921-141">OUTPUTS</span></span>

### <span data-ttu-id="8f921-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8f921-142">System.Boolean</span></span>

## <span data-ttu-id="8f921-143">상속자</span><span class="sxs-lookup"><span data-stu-id="8f921-143">NOTES</span></span>

## <span data-ttu-id="8f921-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f921-144">RELATED LINKS</span></span>

[<span data-ttu-id="8f921-145">새로운 AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8f921-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="8f921-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8f921-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

