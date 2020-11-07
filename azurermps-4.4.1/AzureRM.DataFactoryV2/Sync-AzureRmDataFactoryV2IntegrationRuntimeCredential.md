---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702225"
---
# <span data-ttu-id="73c3a-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="73c3a-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="73c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="73c3a-103">통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73c3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73c3a-104">SYNTAX</span></span>

### <span data-ttu-id="73c3a-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="73c3a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73c3a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="73c3a-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="73c3a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="73c3a-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="73c3a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="73c3a-108">DESCRIPTION</span></span>
<span data-ttu-id="73c3a-109">**AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet은 통합 런타임 노드 간에 온-프레미스 자격 증명을 동기화 하므로 모든 노드에서 자격 증명을 동일 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="73c3a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="73c3a-110">EXAMPLES</span></span>

### <span data-ttu-id="73c3a-111">예제 1: 통합 런타임 자격 증명 동기화</span><span class="sxs-lookup"><span data-stu-id="73c3a-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="73c3a-112">Cmdlet은 통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="73c3a-113">변수</span><span class="sxs-lookup"><span data-stu-id="73c3a-113">PARAMETERS</span></span>

### <span data-ttu-id="73c3a-114">-확인</span><span class="sxs-lookup"><span data-stu-id="73c3a-114">-Confirm</span></span>
<span data-ttu-id="73c3a-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c3a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="73c3a-116">-DataFactoryName</span></span>
<span data-ttu-id="73c3a-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="73c3a-118">-Force</span></span>
<span data-ttu-id="73c3a-119">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="73c3a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73c3a-120">-InputObject</span></span>
<span data-ttu-id="73c3a-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3a-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="73c3a-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="73c3a-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="73c3a-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73c3a-126">-ResourceId</span></span>
<span data-ttu-id="73c3a-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c3a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c3a-128">-WhatIf</span></span>
<span data-ttu-id="73c3a-129">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73c3a-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="73c3a-130">입력</span><span class="sxs-lookup"><span data-stu-id="73c3a-130">INPUTS</span></span>

### <span data-ttu-id="73c3a-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73c3a-131">System.String</span></span>
<span data-ttu-id="73c3a-132">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="73c3a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="73c3a-133">출력</span><span class="sxs-lookup"><span data-stu-id="73c3a-133">OUTPUTS</span></span>

### <span data-ttu-id="73c3a-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="73c3a-134">System.Object</span></span>

## <span data-ttu-id="73c3a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="73c3a-135">NOTES</span></span>

## <span data-ttu-id="73c3a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73c3a-136">RELATED LINKS</span></span>
