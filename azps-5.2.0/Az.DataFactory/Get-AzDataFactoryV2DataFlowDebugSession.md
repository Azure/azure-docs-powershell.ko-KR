---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354465"
---
# <span data-ttu-id="b6bb0-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b6bb0-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b6bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bb0-103">Azure Data Factory에서 모든 활성 데이터 흐름 디버그 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="b6bb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6bb0-104">SYNTAX</span></span>

### <span data-ttu-id="b6bb0-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6bb0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6bb0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6bb0-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6bb0-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b6bb0-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6bb0-108">설명</span><span class="sxs-lookup"><span data-stu-id="b6bb0-108">DESCRIPTION</span></span>
<span data-ttu-id="b6bb0-109">Azure Data Factory의 모든 활성 데이터 흐름 디버그 세션에 세부 정보를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="b6bb0-110">예제</span><span class="sxs-lookup"><span data-stu-id="b6bb0-110">EXAMPLES</span></span>

### <span data-ttu-id="b6bb0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6bb0-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="b6bb0-112">Azure Data Factory "WikiADF"에서 모든 활성 데이터 흐름 디버그 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="b6bb0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bb0-113">PARAMETERS</span></span>

### <span data-ttu-id="b6bb0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6bb0-114">-DataFactory</span></span>
<span data-ttu-id="b6bb0-115">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bb0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b6bb0-116">-DataFactoryName</span></span>
<span data-ttu-id="b6bb0-117">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bb0-118">-DefaultProfile</span></span>
<span data-ttu-id="b6bb0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bb0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bb0-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6bb0-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bb0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6bb0-122">-ResourceId</span></span>
<span data-ttu-id="b6bb0-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bb0-124">CommonParameters</span></span>
<span data-ttu-id="b6bb0-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bb0-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6bb0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bb0-127">입력</span><span class="sxs-lookup"><span data-stu-id="b6bb0-127">INPUTS</span></span>

### <span data-ttu-id="b6bb0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b6bb0-128">System.String</span></span>

### <span data-ttu-id="b6bb0-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b6bb0-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b6bb0-130">출력</span><span class="sxs-lookup"><span data-stu-id="b6bb0-130">OUTPUTS</span></span>

### <span data-ttu-id="b6bb0-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="b6bb0-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="b6bb0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6bb0-132">NOTES</span></span>
<span data-ttu-id="b6bb0-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="b6bb0-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b6bb0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6bb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6bb0-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b6bb0-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b6bb0-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b6bb0-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="b6bb0-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="b6bb0-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="b6bb0-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b6bb0-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)