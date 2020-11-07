---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: 9a2449299c6c4a6d87ee7c4b0403a35a0b7c3683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698517"
---
# <span data-ttu-id="135ab-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="135ab-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="135ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="135ab-102">SYNOPSIS</span></span>
<span data-ttu-id="135ab-103">지정 된 대상 파일에 대 한 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="135ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="135ab-104">SYNTAX</span></span>

### <span data-ttu-id="135ab-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="135ab-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="135ab-106">파일</span><span class="sxs-lookup"><span data-stu-id="135ab-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="135ab-107">설명은</span><span class="sxs-lookup"><span data-stu-id="135ab-107">DESCRIPTION</span></span>
<span data-ttu-id="135ab-108">**AzStorageFileCopy** cmdlet은 대상 파일에 대 한 파일 복사를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="135ab-109">예제의</span><span class="sxs-lookup"><span data-stu-id="135ab-109">EXAMPLES</span></span>

### <span data-ttu-id="135ab-110">예제 1: 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="135ab-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="135ab-111">이 명령은 지정 된 이름을 가진 파일의 복사를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="135ab-112">변수</span><span class="sxs-lookup"><span data-stu-id="135ab-112">PARAMETERS</span></span>

### <span data-ttu-id="135ab-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="135ab-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="135ab-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="135ab-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="135ab-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="135ab-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="135ab-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="135ab-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="135ab-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="135ab-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="135ab-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="135ab-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-122">The default value is 10.</span></span>

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

### <span data-ttu-id="135ab-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="135ab-123">-Context</span></span>
<span data-ttu-id="135ab-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="135ab-125">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="135ab-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="135ab-126">-CopyId</span></span>
<span data-ttu-id="135ab-127">복사 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135ab-128">-DefaultProfile</span></span>
<span data-ttu-id="135ab-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ab-130">-파일</span><span class="sxs-lookup"><span data-stu-id="135ab-130">-File</span></span>
<span data-ttu-id="135ab-131">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="135ab-132">클라우드 파일을 만들거나 Get-AzStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="135ab-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="135ab-133">-FilePath</span></span>
<span data-ttu-id="135ab-134">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="135ab-135">-Force</span><span class="sxs-lookup"><span data-stu-id="135ab-135">-Force</span></span>
<span data-ttu-id="135ab-136">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="135ab-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="135ab-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="135ab-138">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="135ab-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="135ab-139">-ShareName</span></span>
<span data-ttu-id="135ab-140">공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="135ab-141">-확인</span><span class="sxs-lookup"><span data-stu-id="135ab-141">-Confirm</span></span>
<span data-ttu-id="135ab-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ab-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="135ab-143">-WhatIf</span></span>
<span data-ttu-id="135ab-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="135ab-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135ab-146">CommonParameters</span></span>
<span data-ttu-id="135ab-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135ab-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="135ab-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135ab-149">입력</span><span class="sxs-lookup"><span data-stu-id="135ab-149">INPUTS</span></span>

### <span data-ttu-id="135ab-150">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="135ab-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="135ab-151">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="135ab-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="135ab-152">출력</span><span class="sxs-lookup"><span data-stu-id="135ab-152">OUTPUTS</span></span>

### <span data-ttu-id="135ab-153">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="135ab-153">System.Void</span></span>

## <span data-ttu-id="135ab-154">상속자</span><span class="sxs-lookup"><span data-stu-id="135ab-154">NOTES</span></span>

## <span data-ttu-id="135ab-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="135ab-155">RELATED LINKS</span></span>

[<span data-ttu-id="135ab-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="135ab-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="135ab-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="135ab-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="135ab-158">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="135ab-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="135ab-159">시작-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="135ab-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
