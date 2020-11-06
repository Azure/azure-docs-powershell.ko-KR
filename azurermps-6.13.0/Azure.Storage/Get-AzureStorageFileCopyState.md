---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
ms.openlocfilehash: 811e642bf92e12c0d385ff38d93297c3a7c060ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529672"
---
# <span data-ttu-id="3aaf9-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="3aaf9-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="3aaf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aaf9-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaf9-103">복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aaf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3aaf9-104">SYNTAX</span></span>

### <span data-ttu-id="3aaf9-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="3aaf9-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3aaf9-106">파일</span><span class="sxs-lookup"><span data-stu-id="3aaf9-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3aaf9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3aaf9-107">DESCRIPTION</span></span>
<span data-ttu-id="3aaf9-108">**AzureStorageFileCopyState** Cmdlet은 Azure 저장소 파일 복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="3aaf9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3aaf9-109">EXAMPLES</span></span>

### <span data-ttu-id="3aaf9-110">예제 1: 파일 이름으로 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="3aaf9-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="3aaf9-111">이 명령은 지정 된 이름을 가진 파일에 대 한 복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="3aaf9-112">변수</span><span class="sxs-lookup"><span data-stu-id="3aaf9-112">PARAMETERS</span></span>

### <span data-ttu-id="3aaf9-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3aaf9-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3aaf9-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3aaf9-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3aaf9-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3aaf9-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3aaf9-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3aaf9-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3aaf9-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3aaf9-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3aaf9-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3aaf9-123">-Context</span></span>
<span data-ttu-id="3aaf9-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3aaf9-125">컨텍스트를 가져오려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaf9-126">-DefaultProfile</span></span>
<span data-ttu-id="3aaf9-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-128">-파일</span><span class="sxs-lookup"><span data-stu-id="3aaf9-128">-File</span></span>
<span data-ttu-id="3aaf9-129">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3aaf9-130">클라우드 파일을 만들거나 Get-AzureStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3aaf9-131">-FilePath</span></span>
<span data-ttu-id="3aaf9-132">Azure 저장소 공유에 상대적인 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3aaf9-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3aaf9-134">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-134">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3aaf9-135">-ShareName</span></span>
<span data-ttu-id="3aaf9-136">공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-136">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf9-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="3aaf9-137">-WaitForComplete</span></span>
<span data-ttu-id="3aaf9-138">이 cmdlet이 복사가 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="3aaf9-139">이 매개 변수를 지정 하지 않으면이 cmdlet은 결과를 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="3aaf9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaf9-140">CommonParameters</span></span>
<span data-ttu-id="3aaf9-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaf9-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aaf9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaf9-143">입력</span><span class="sxs-lookup"><span data-stu-id="3aaf9-143">INPUTS</span></span>

### <span data-ttu-id="3aaf9-144">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="3aaf9-145">매개 변수: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3aaf9-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="3aaf9-146">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3aaf9-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3aaf9-147">출력</span><span class="sxs-lookup"><span data-stu-id="3aaf9-147">OUTPUTS</span></span>

### <span data-ttu-id="3aaf9-148">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aaf9-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="3aaf9-149">상속자</span><span class="sxs-lookup"><span data-stu-id="3aaf9-149">NOTES</span></span>

## <span data-ttu-id="3aaf9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3aaf9-150">RELATED LINKS</span></span>

[<span data-ttu-id="3aaf9-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3aaf9-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3aaf9-152">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3aaf9-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3aaf9-153">시작-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3aaf9-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="3aaf9-154">중지-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3aaf9-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
