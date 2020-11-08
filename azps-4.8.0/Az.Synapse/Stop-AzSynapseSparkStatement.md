---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047465"
---
# <span data-ttu-id="7c91a-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="7c91a-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="7c91a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c91a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c91a-103">Synapse Analytics Spark 문을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="7c91a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c91a-104">SYNTAX</span></span>

### <span data-ttu-id="7c91a-105">StopSparkStatementByIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c91a-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c91a-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c91a-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c91a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c91a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c91a-108">**AzSynapseSparkStatement** Cmdlet은 Synapse Analytics Spark 문을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="7c91a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c91a-109">EXAMPLES</span></span>

### <span data-ttu-id="7c91a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c91a-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="7c91a-111">이 명령은 지정 된 livy ID의 Spark 문을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="7c91a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c91a-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="7c91a-113">이 명령은 지정 된 livy ID를 통해 파이프라인을 사용 하 여 Spark 문을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="7c91a-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c91a-114">PARAMETERS</span></span>

### <span data-ttu-id="7c91a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c91a-115">-DefaultProfile</span></span>
<span data-ttu-id="7c91a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c91a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7c91a-117">-Force</span></span>
<span data-ttu-id="7c91a-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7c91a-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="7c91a-119">-LivyId</span></span>
<span data-ttu-id="7c91a-120">Spark 문의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c91a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c91a-121">-PassThru</span></span>
<span data-ttu-id="7c91a-122">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7c91a-123">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c91a-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="7c91a-124">-SessionId</span></span>
<span data-ttu-id="7c91a-125">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c91a-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="7c91a-126">-SessionObject</span></span>
<span data-ttu-id="7c91a-127">일반적으로 파이프라인을 통해 전달 되는 Spark 세션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c91a-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="7c91a-128">-SparkPoolName</span></span>
<span data-ttu-id="7c91a-129">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c91a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c91a-130">-WorkspaceName</span></span>
<span data-ttu-id="7c91a-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c91a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7c91a-132">-Confirm</span></span>
<span data-ttu-id="7c91a-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c91a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c91a-134">-WhatIf</span></span>
<span data-ttu-id="7c91a-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c91a-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c91a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c91a-137">CommonParameters</span></span>
<span data-ttu-id="7c91a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c91a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c91a-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c91a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c91a-140">입력</span><span class="sxs-lookup"><span data-stu-id="7c91a-140">INPUTS</span></span>

### <span data-ttu-id="7c91a-141">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="7c91a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="7c91a-142">출력</span><span class="sxs-lookup"><span data-stu-id="7c91a-142">OUTPUTS</span></span>

### <span data-ttu-id="7c91a-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7c91a-143">System.Boolean</span></span>

## <span data-ttu-id="7c91a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="7c91a-144">NOTES</span></span>

## <span data-ttu-id="7c91a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c91a-145">RELATED LINKS</span></span>
