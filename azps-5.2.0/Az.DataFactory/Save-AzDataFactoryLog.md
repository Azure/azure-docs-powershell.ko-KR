---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365688"
---
# <span data-ttu-id="a06a9-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="a06a9-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="a06a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a06a9-103">Azure HDInsight 처리에서 로그 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="a06a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a06a9-104">SYNTAX</span></span>

### <span data-ttu-id="a06a9-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a06a9-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06a9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a06a9-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="a06a9-107">DESCRIPTION</span></span>
<span data-ttu-id="a06a9-108">**Save-AzDataFactoryLog** cmdlet은 Pig 또는 Hive 프로젝트의 Azure HDInsight 처리 또는 사용자 지정 작업을 로컬 하드 드라이브에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="a06a9-109">먼저 Get-AzDataFactoryRun cmdlet을 실행하여 데이터 조각에 대한 활동 실행 ID를 가져온 다음 해당 ID를 사용하여 HDInsight 클러스터와 연결된 BLOB(이진 큰 개체) 저장소에서 로그 파일을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="a06a9-110">*DownloadLogs* 매개 변수를 지정하지 않으면 cmdlet은 로그 파일의 위치만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="a06a9-111">출력 디렉터리(출력 매개 변수)를 지정하지 않고 *DownloadLogs를* 지정하면 로그 파일이 기본 문서 폴더에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="a06a9-112">출력 폴더(출력)와 함께 *DownloadLogs를* 지정하면 로그 파일이 지정된 폴더에 다운로드됩니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="a06a9-113">예제</span><span class="sxs-lookup"><span data-stu-id="a06a9-113">EXAMPLES</span></span>

### <span data-ttu-id="a06a9-114">예제 1: 로그 파일을 특정 폴더에 저장</span><span class="sxs-lookup"><span data-stu-id="a06a9-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="a06a9-115">이 명령은 ID가 841b77c9-d56c-48d1-99a3-8c16c3e77d39인 활동 실행에 대한 로그 파일을 저장합니다. 여기서 활동은 ADF라는 리소스 그룹의 LogProcessingFactory라는 데이터 팩터리의 파이프라인에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="a06a9-116">로그 파일은 C:\Test 폴더에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="a06a9-117">예제 2: 기본 문서 폴더에 로그 파일 저장</span><span class="sxs-lookup"><span data-stu-id="a06a9-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="a06a9-118">이 명령은 로그 파일을 문서 폴더(기본값)에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="a06a9-119">예제 3: 로그 파일의 위치 확인</span><span class="sxs-lookup"><span data-stu-id="a06a9-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="a06a9-120">이 명령은 로그 파일의 위치를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-120">This command returns the location of log files.</span></span>
<span data-ttu-id="a06a9-121">*DownloadLogs는* 지정되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="a06a9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a06a9-122">PARAMETERS</span></span>

### <span data-ttu-id="a06a9-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a06a9-123">-DataFactory</span></span>
<span data-ttu-id="a06a9-124">**PSDataFactory 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a06a9-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a06a9-125">-DataFactoryName</span></span>
<span data-ttu-id="a06a9-126">데이터 팩터리의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a06a9-127">이 cmdlet은 이 매개 변수가 지정하는 데이터 팩터리에 대한 로그 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a06a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06a9-128">-DefaultProfile</span></span>
<span data-ttu-id="a06a9-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a06a9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a06a9-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="a06a9-130">-DownloadLogs</span></span>
<span data-ttu-id="a06a9-131">이 cmdlet이 로그 파일을 로컬 컴퓨터에 다운로드하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="a06a9-132">출력 *폴더를* 지정하지 않으면 파일이 하위 폴더 아래에 문서 폴더에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="a06a9-133">-Id</span><span class="sxs-lookup"><span data-stu-id="a06a9-133">-Id</span></span>
<span data-ttu-id="a06a9-134">데이터 조각에 대한 활동 실행의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="a06a9-135">id를 Get-AzDataFactoryRun cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-136">-Output</span><span class="sxs-lookup"><span data-stu-id="a06a9-136">-Output</span></span>
<span data-ttu-id="a06a9-137">다운로드한 로그 파일이 저장되는 출력 폴더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06a9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06a9-138">-ResourceGroupName</span></span>
<span data-ttu-id="a06a9-139">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a06a9-140">이 cmdlet은 이 매개 변수가 지정하는 그룹에 속하는 데이터 팩터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a06a9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06a9-141">CommonParameters</span></span>
<span data-ttu-id="a06a9-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a06a9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06a9-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a06a9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06a9-144">입력</span><span class="sxs-lookup"><span data-stu-id="a06a9-144">INPUTS</span></span>

### <span data-ttu-id="a06a9-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a06a9-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a06a9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a06a9-146">System.String</span></span>

## <span data-ttu-id="a06a9-147">출력</span><span class="sxs-lookup"><span data-stu-id="a06a9-147">OUTPUTS</span></span>

### <span data-ttu-id="a06a9-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="a06a9-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="a06a9-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a06a9-149">NOTES</span></span>
* <span data-ttu-id="a06a9-150">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="a06a9-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a06a9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a06a9-151">RELATED LINKS</span></span>

[<span data-ttu-id="a06a9-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a06a9-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="a06a9-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a06a9-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="a06a9-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a06a9-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="a06a9-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a06a9-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="a06a9-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a06a9-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a06a9-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a06a9-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


