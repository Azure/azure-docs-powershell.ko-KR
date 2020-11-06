---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 058c923528227e05a4c8b8078f4495c56edfe20c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526900"
---
# <span data-ttu-id="4203c-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="4203c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4203c-102">SYNOPSIS</span></span>
<span data-ttu-id="4203c-103">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4203c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4203c-104">SYNTAX</span></span>

### <span data-ttu-id="4203c-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4203c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4203c-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4203c-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4203c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4203c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4203c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4203c-108">DESCRIPTION</span></span>
<span data-ttu-id="4203c-109">Remove-AzureRmContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="4203c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4203c-110">EXAMPLES</span></span>

### <span data-ttu-id="4203c-111">예제 1: 컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="4203c-112">컨테이너 레지스트리 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="4203c-113">변수</span><span class="sxs-lookup"><span data-stu-id="4203c-113">PARAMETERS</span></span>

### <span data-ttu-id="4203c-114">-확인</span><span class="sxs-lookup"><span data-stu-id="4203c-114">-Confirm</span></span>
<span data-ttu-id="4203c-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4203c-116">-DefaultProfile</span></span>
<span data-ttu-id="4203c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4203c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4203c-118">-Name</span></span>
<span data-ttu-id="4203c-119">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="4203c-119">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4203c-120">-RegistryName</span></span>
<span data-ttu-id="4203c-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4203c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4203c-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4203c-124">-ResourceId</span></span>
<span data-ttu-id="4203c-125">컨테이너 레지스트리 Webhook 리소스 id</span><span class="sxs-lookup"><span data-stu-id="4203c-125">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="4203c-126">-Webhook</span></span>
<span data-ttu-id="4203c-127">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4203c-128">-WhatIf</span></span>
<span data-ttu-id="4203c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4203c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4203c-131">-PassThru</span></span>
<span data-ttu-id="4203c-132">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-132">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4203c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4203c-133">CommonParameters</span></span>
<span data-ttu-id="4203c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4203c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4203c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4203c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4203c-136">입력</span><span class="sxs-lookup"><span data-stu-id="4203c-136">INPUTS</span></span>

### <span data-ttu-id="4203c-137">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="4203c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4203c-138">System.String</span></span>

## <span data-ttu-id="4203c-139">출력</span><span class="sxs-lookup"><span data-stu-id="4203c-139">OUTPUTS</span></span>

### <span data-ttu-id="4203c-140">System. 개체</span><span class="sxs-lookup"><span data-stu-id="4203c-140">System.Object</span></span>

## <span data-ttu-id="4203c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4203c-141">NOTES</span></span>

## <span data-ttu-id="4203c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4203c-142">RELATED LINKS</span></span>

[<span data-ttu-id="4203c-143">새로운 AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-143">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4203c-144">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-144">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4203c-145">업데이트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-145">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="4203c-146">테스트-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4203c-146">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
