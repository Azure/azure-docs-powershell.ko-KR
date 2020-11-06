---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527059"
---
# <span data-ttu-id="726d3-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="726d3-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="726d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726d3-102">SYNOPSIS</span></span>
<span data-ttu-id="726d3-103">일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="726d3-104">SYNTAX</span></span>

### <span data-ttu-id="726d3-105">I</span><span class="sxs-lookup"><span data-stu-id="726d3-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="726d3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="726d3-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="726d3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="726d3-107">DESCRIPTION</span></span>
<span data-ttu-id="726d3-108">**Stop-AzureBatchTask** Cmdlet은 Azure 일괄 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="726d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="726d3-109">EXAMPLES</span></span>

### <span data-ttu-id="726d3-110">예제 1: ID를 기준으로 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="726d3-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="726d3-111">이 명령은 ID 작업이 있는 작업 아래에 id Task23 인 작업을 중지 합니다-000001.</span><span class="sxs-lookup"><span data-stu-id="726d3-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="726d3-112">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="726d3-113">Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="726d3-114">예제 2: 파이프라인을 사용 하 여 일괄 작업 중지</span><span class="sxs-lookup"><span data-stu-id="726d3-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="726d3-115">이 명령은 Get-AzureBatchTask cmdlet을 사용 하 여 ID 작업이 있는 작업에서 ID Task26 인 일괄 처리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="726d3-116">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="726d3-117">명령이 해당 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-117">The command stops that task.</span></span>

## <span data-ttu-id="726d3-118">변수</span><span class="sxs-lookup"><span data-stu-id="726d3-118">PARAMETERS</span></span>

### <span data-ttu-id="726d3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="726d3-119">-BatchContext</span></span>
<span data-ttu-id="726d3-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="726d3-121">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="726d3-122">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="726d3-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="726d3-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726d3-125">-DefaultProfile</span></span>
<span data-ttu-id="726d3-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726d3-127">-Id</span><span class="sxs-lookup"><span data-stu-id="726d3-127">-Id</span></span>
<span data-ttu-id="726d3-128">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="726d3-129">-JobId</span></span>
<span data-ttu-id="726d3-130">작업을 포함 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-131">-작업</span><span class="sxs-lookup"><span data-stu-id="726d3-131">-Task</span></span>
<span data-ttu-id="726d3-132">이 cmdlet이 중지 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="726d3-133">**Pscloudtask** 개체를 가져오려면 Get-AzureBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="726d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726d3-134">CommonParameters</span></span>
<span data-ttu-id="726d3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726d3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726d3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726d3-137">입력</span><span class="sxs-lookup"><span data-stu-id="726d3-137">INPUTS</span></span>

### <span data-ttu-id="726d3-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="726d3-138">BatchAccountContext</span></span>
<span data-ttu-id="726d3-139">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="726d3-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="726d3-140">PSCloudTask</span></span>
<span data-ttu-id="726d3-141">' Task ' 매개 변수는 파이프라인에서 ' PSCloudTask ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="726d3-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="726d3-142">출력</span><span class="sxs-lookup"><span data-stu-id="726d3-142">OUTPUTS</span></span>

## <span data-ttu-id="726d3-143">상속자</span><span class="sxs-lookup"><span data-stu-id="726d3-143">NOTES</span></span>

## <span data-ttu-id="726d3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="726d3-144">RELATED LINKS</span></span>

[<span data-ttu-id="726d3-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="726d3-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="726d3-146">새-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="726d3-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="726d3-147">-AzureBatchTask 제거</span><span class="sxs-lookup"><span data-stu-id="726d3-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="726d3-148">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="726d3-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


