---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212832"
---
# <span data-ttu-id="94a96-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="94a96-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="94a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a96-102">SYNOPSIS</span></span>
<span data-ttu-id="94a96-103">Azure Data Factory에서 데이터 흐름 디버그 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="94a96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94a96-104">SYNTAX</span></span>

### <span data-ttu-id="94a96-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="94a96-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94a96-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="94a96-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a96-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94a96-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a96-108">설명은</span><span class="sxs-lookup"><span data-stu-id="94a96-108">DESCRIPTION</span></span>
<span data-ttu-id="94a96-109">이 명령은 디버그 세션을 중지 하 고, 그렇지 않으면 디버그 세션의 시간 대 라이브 설정에 따라 세션이 자동으로 해제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="94a96-110">예제의</span><span class="sxs-lookup"><span data-stu-id="94a96-110">EXAMPLES</span></span>

### <span data-ttu-id="94a96-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="94a96-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="94a96-112">Data factory "WikiADF"에서 데이터 흐름 디버그 세션 "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d"을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="94a96-113">변수</span><span class="sxs-lookup"><span data-stu-id="94a96-113">PARAMETERS</span></span>

### <span data-ttu-id="94a96-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="94a96-114">-DataFactory</span></span>
<span data-ttu-id="94a96-115">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-115">The data factory object.</span></span>

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

### <span data-ttu-id="94a96-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="94a96-116">-DataFactoryName</span></span>
<span data-ttu-id="94a96-117">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-117">The data factory name.</span></span>

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

### <span data-ttu-id="94a96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a96-118">-DefaultProfile</span></span>
<span data-ttu-id="94a96-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a96-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94a96-120">-PassThru</span></span>
<span data-ttu-id="94a96-121">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="94a96-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="94a96-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a96-123">-ResourceGroupName</span></span>
<span data-ttu-id="94a96-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-124">The resource group name.</span></span>

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

### <span data-ttu-id="94a96-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a96-125">-ResourceId</span></span>
<span data-ttu-id="94a96-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="94a96-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="94a96-127">-SessionId</span></span>
<span data-ttu-id="94a96-128">데이터 흐름 디버그 세션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a96-129">-확인</span><span class="sxs-lookup"><span data-stu-id="94a96-129">-Confirm</span></span>
<span data-ttu-id="94a96-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a96-131">-WhatIf</span></span>
<span data-ttu-id="94a96-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a96-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a96-134">CommonParameters</span></span>
<span data-ttu-id="94a96-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94a96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a96-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94a96-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a96-137">입력</span><span class="sxs-lookup"><span data-stu-id="94a96-137">INPUTS</span></span>

### <span data-ttu-id="94a96-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94a96-138">System.String</span></span>

### <span data-ttu-id="94a96-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="94a96-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="94a96-140">출력</span><span class="sxs-lookup"><span data-stu-id="94a96-140">OUTPUTS</span></span>

### <span data-ttu-id="94a96-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="94a96-141">System.Void</span></span>

### <span data-ttu-id="94a96-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="94a96-142">System.Boolean</span></span>

## <span data-ttu-id="94a96-143">상속자</span><span class="sxs-lookup"><span data-stu-id="94a96-143">NOTES</span></span>
<span data-ttu-id="94a96-144">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="94a96-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="94a96-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94a96-145">RELATED LINKS</span></span>

[<span data-ttu-id="94a96-146">시작-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="94a96-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="94a96-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="94a96-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="94a96-148">추가-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="94a96-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="94a96-149">AzDataFactoryV2DataFlowDebugSessionCommand-호출</span><span class="sxs-lookup"><span data-stu-id="94a96-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)