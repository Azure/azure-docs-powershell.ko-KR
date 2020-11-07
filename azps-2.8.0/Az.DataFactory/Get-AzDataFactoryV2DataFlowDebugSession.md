---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 1521f0f4f3b90010e24185a036dca047860e27c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697063"
---
# <span data-ttu-id="03a02-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="03a02-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="03a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a02-102">SYNOPSIS</span></span>
<span data-ttu-id="03a02-103">Azure Data Factory에서 모든 활성 데이터 흐름 디버그 세션 가져오기</span><span class="sxs-lookup"><span data-stu-id="03a02-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="03a02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03a02-104">SYNTAX</span></span>

### <span data-ttu-id="03a02-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="03a02-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03a02-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03a02-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03a02-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="03a02-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03a02-108">설명은</span><span class="sxs-lookup"><span data-stu-id="03a02-108">DESCRIPTION</span></span>
<span data-ttu-id="03a02-109">자세한 내용은 Azure Data Factory에서 모든 활성 데이터 흐름 디버그 세션을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="03a02-110">예제의</span><span class="sxs-lookup"><span data-stu-id="03a02-110">EXAMPLES</span></span>

### <span data-ttu-id="03a02-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="03a02-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="03a02-112">Azure Data Factory "WikiADF"에서 모든 활성 데이터 흐름 디버그 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="03a02-113">변수</span><span class="sxs-lookup"><span data-stu-id="03a02-113">PARAMETERS</span></span>

### <span data-ttu-id="03a02-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="03a02-114">-DataFactory</span></span>
<span data-ttu-id="03a02-115">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-115">The data factory object.</span></span>

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

### <span data-ttu-id="03a02-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="03a02-116">-DataFactoryName</span></span>
<span data-ttu-id="03a02-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-117">The data factory name.</span></span>

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

### <span data-ttu-id="03a02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a02-118">-DefaultProfile</span></span>
<span data-ttu-id="03a02-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a02-120">-ResourceGroupName</span></span>
<span data-ttu-id="03a02-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-121">The resource group name.</span></span>

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

### <span data-ttu-id="03a02-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03a02-122">-ResourceId</span></span>
<span data-ttu-id="03a02-123">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03a02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a02-124">CommonParameters</span></span>
<span data-ttu-id="03a02-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a02-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="03a02-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a02-127">입력</span><span class="sxs-lookup"><span data-stu-id="03a02-127">INPUTS</span></span>

### <span data-ttu-id="03a02-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03a02-128">System.String</span></span>

### <span data-ttu-id="03a02-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="03a02-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="03a02-130">출력</span><span class="sxs-lookup"><span data-stu-id="03a02-130">OUTPUTS</span></span>

### <span data-ttu-id="03a02-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="03a02-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="03a02-132">상속자</span><span class="sxs-lookup"><span data-stu-id="03a02-132">NOTES</span></span>
<span data-ttu-id="03a02-133">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="03a02-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="03a02-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03a02-134">RELATED LINKS</span></span>

[<span data-ttu-id="03a02-135">시작-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="03a02-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="03a02-136">추가-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="03a02-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="03a02-137">AzDataFactoryV2DataFlowDebugSessionCommand-호출</span><span class="sxs-lookup"><span data-stu-id="03a02-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="03a02-138">중지-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="03a02-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)