---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: cb9362a64b58770beb7d3b70f989fc740a2fc00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879313"
---
# <span data-ttu-id="97e6c-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="97e6c-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="97e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="97e6c-103">통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="97e6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97e6c-104">SYNTAX</span></span>

### <span data-ttu-id="97e6c-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="97e6c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e6c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97e6c-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e6c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="97e6c-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e6c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="97e6c-108">DESCRIPTION</span></span>
<span data-ttu-id="97e6c-109">**AzDataFactoryV2IntegrationRuntimeCredential** cmdlet은 통합 런타임 노드 간에 온-프레미스 자격 증명을 동기화 하므로 모든 노드에서 자격 증명을 동일 하 게 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="97e6c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="97e6c-110">EXAMPLES</span></span>

### <span data-ttu-id="97e6c-111">예제 1: 통합 런타임 자격 증명 동기화</span><span class="sxs-lookup"><span data-stu-id="97e6c-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="97e6c-112">Cmdlet은 통합 런타임 노드 간에 자격 증명을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="97e6c-113">변수</span><span class="sxs-lookup"><span data-stu-id="97e6c-113">PARAMETERS</span></span>

### <span data-ttu-id="97e6c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="97e6c-114">-DataFactoryName</span></span>
<span data-ttu-id="97e6c-115">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e6c-116">-DefaultProfile</span></span>
<span data-ttu-id="97e6c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97e6c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="97e6c-118">-Force</span></span>
<span data-ttu-id="97e6c-119">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="97e6c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97e6c-120">-InputObject</span></span>
<span data-ttu-id="97e6c-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97e6c-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="97e6c-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="97e6c-123">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="97e6c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e6c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97e6c-126">-ResourceId</span></span>
<span data-ttu-id="97e6c-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e6c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="97e6c-128">-Confirm</span></span>
<span data-ttu-id="97e6c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e6c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e6c-130">-WhatIf</span></span>
<span data-ttu-id="97e6c-131">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="97e6c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e6c-132">CommonParameters</span></span>
<span data-ttu-id="97e6c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e6c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e6c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e6c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e6c-135">입력</span><span class="sxs-lookup"><span data-stu-id="97e6c-135">INPUTS</span></span>

### <span data-ttu-id="97e6c-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="97e6c-136">System.String</span></span>

### <span data-ttu-id="97e6c-137">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="97e6c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="97e6c-138">출력</span><span class="sxs-lookup"><span data-stu-id="97e6c-138">OUTPUTS</span></span>

### <span data-ttu-id="97e6c-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="97e6c-139">System.Void</span></span>

## <span data-ttu-id="97e6c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="97e6c-140">NOTES</span></span>

## <span data-ttu-id="97e6c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97e6c-141">RELATED LINKS</span></span>
