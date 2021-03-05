---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: 185f01f31f8cae62e51b7b28909f66fbf37884e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992810"
---
# <span data-ttu-id="cbd79-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cbd79-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="cbd79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd79-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd79-103">특정 데이터 흐름 디버그 세션에 데이터 흐름 리소스 및 해당 종속성 추가</span><span class="sxs-lookup"><span data-stu-id="cbd79-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="cbd79-104">구문</span><span class="sxs-lookup"><span data-stu-id="cbd79-104">SYNTAX</span></span>

### <span data-ttu-id="cbd79-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cbd79-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd79-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cbd79-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbd79-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd79-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd79-108">설명</span><span class="sxs-lookup"><span data-stu-id="cbd79-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd79-109">이 명령은 데이터 흐름 리소스 및 해당 종속성은 데이터 흐름 디버그 워크플로에 대한 PowerShell 명령 시퀀스를 특정 디버그 세션에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="cbd79-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbd79-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="cbd79-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="cbd79-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="cbd79-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand(다른 명령/대상에 대해 이 단계를 반복하거나 패키지 파일을 변경하기 위해 2-3단계를 반복)</span><span class="sxs-lookup"><span data-stu-id="cbd79-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="cbd79-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbd79-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="cbd79-114">예제</span><span class="sxs-lookup"><span data-stu-id="cbd79-114">EXAMPLES</span></span>

### <span data-ttu-id="cbd79-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="cbd79-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="cbd79-116">"WikiADF" 데이터 팩터리의 디버그 세션 "550effe4-93a3-485c-8525-eaf25259efbd"에 데이터 흐름 패키지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="cbd79-117">Pakcage 파일에는 데이터 흐름 디버그 리소스, 데이터 세트 디버그 다시 사용 목록, 연결된 서비스 디버그 리소스 목록, 디버그 설정 및 세션 ID가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="cbd79-118">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="cbd79-118">For instance:</span></span>

<span data-ttu-id="cbd79-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } } ] "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000} } }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="cbd79-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="cbd79-120">SessionID 매개 변수는 패키지 파일의 기존 sessionId 속성을 대체하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="cbd79-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cbd79-121">PARAMETERS</span></span>

### <span data-ttu-id="cbd79-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cbd79-122">-DataFactory</span></span>
<span data-ttu-id="cbd79-123">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-123">The data factory object.</span></span>

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

### <span data-ttu-id="cbd79-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cbd79-124">-DataFactoryName</span></span>
<span data-ttu-id="cbd79-125">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-125">The data factory name.</span></span>

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

### <span data-ttu-id="cbd79-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd79-126">-DefaultProfile</span></span>
<span data-ttu-id="cbd79-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd79-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="cbd79-128">-PackageFile</span></span>
<span data-ttu-id="cbd79-129">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd79-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbd79-130">-PassThru</span></span>
<span data-ttu-id="cbd79-131">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="cbd79-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="cbd79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd79-133">-ResourceGroupName</span></span>
<span data-ttu-id="cbd79-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-134">The resource group name.</span></span>

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

### <span data-ttu-id="cbd79-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd79-135">-ResourceId</span></span>
<span data-ttu-id="cbd79-136">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cbd79-137">-확인</span><span class="sxs-lookup"><span data-stu-id="cbd79-137">-Confirm</span></span>
<span data-ttu-id="cbd79-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd79-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd79-139">-WhatIf</span></span>
<span data-ttu-id="cbd79-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd79-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd79-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd79-142">CommonParameters</span></span>
<span data-ttu-id="cbd79-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cbd79-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd79-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbd79-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd79-145">입력</span><span class="sxs-lookup"><span data-stu-id="cbd79-145">INPUTS</span></span>

### <span data-ttu-id="cbd79-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cbd79-146">System.String</span></span>

### <span data-ttu-id="cbd79-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cbd79-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cbd79-148">출력</span><span class="sxs-lookup"><span data-stu-id="cbd79-148">OUTPUTS</span></span>

### <span data-ttu-id="cbd79-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="cbd79-149">System.Void</span></span>

### <span data-ttu-id="cbd79-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbd79-150">System.Boolean</span></span>

## <span data-ttu-id="cbd79-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cbd79-151">NOTES</span></span>
<span data-ttu-id="cbd79-152">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="cbd79-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cbd79-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbd79-153">RELATED LINKS</span></span>

[<span data-ttu-id="cbd79-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbd79-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cbd79-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbd79-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="cbd79-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="cbd79-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="cbd79-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cbd79-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
