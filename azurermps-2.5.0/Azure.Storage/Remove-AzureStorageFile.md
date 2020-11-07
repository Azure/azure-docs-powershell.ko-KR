---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
ms.openlocfilehash: cfb5a3255a91c7a7206ba0729c20e4d0c68c3ea2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882729"
---
# <span data-ttu-id="1c376-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1c376-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="1c376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c376-102">SYNOPSIS</span></span>
<span data-ttu-id="1c376-103">파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c376-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c376-104">SYNTAX</span></span>

### <span data-ttu-id="1c376-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1c376-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c376-106">공유</span><span class="sxs-lookup"><span data-stu-id="1c376-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c376-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="1c376-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c376-108">파일</span><span class="sxs-lookup"><span data-stu-id="1c376-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c376-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1c376-109">DESCRIPTION</span></span>
<span data-ttu-id="1c376-110">**제거-AzureStorageFile** cmdlet은 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="1c376-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1c376-111">EXAMPLES</span></span>

### <span data-ttu-id="1c376-112">예제 1: 파일 공유에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="1c376-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="1c376-113">이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1c376-114">예제 2: 파일 공유 개체를 사용 하 여 파일 공유에서 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="1c376-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="1c376-115">이 명령은 **AzureStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1c376-116">현재 명령은 ContosoShare06에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="1c376-117">변수</span><span class="sxs-lookup"><span data-stu-id="1c376-117">PARAMETERS</span></span>

### <span data-ttu-id="1c376-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c376-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1c376-119">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1c376-120">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1c376-121">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1c376-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1c376-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1c376-123">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1c376-124">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1c376-125">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1c376-126">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1c376-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-127">The default value is 10.</span></span>

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

### <span data-ttu-id="1c376-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1c376-128">-Context</span></span>
<span data-ttu-id="1c376-129">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1c376-130">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1c376-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c376-131">-DefaultProfile</span></span>
<span data-ttu-id="1c376-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c376-133">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="1c376-133">-Directory</span></span>
<span data-ttu-id="1c376-134">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1c376-135">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c376-136">-파일</span><span class="sxs-lookup"><span data-stu-id="1c376-136">-File</span></span>
<span data-ttu-id="1c376-137">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="1c376-138">이 cmdlet은이 매개 변수에서 지정 하는 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="1c376-139">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-139">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1c376-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c376-140">-PassThru</span></span>
<span data-ttu-id="1c376-141">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1c376-142">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1c376-143">-Path</span><span class="sxs-lookup"><span data-stu-id="1c376-143">-Path</span></span>
<span data-ttu-id="1c376-144">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-144">Specifies the path of a file.</span></span>
<span data-ttu-id="1c376-145">이 cmdlet은이 매개 변수에서 지정 하는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c376-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1c376-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1c376-147">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1c376-148">-공유</span><span class="sxs-lookup"><span data-stu-id="1c376-148">-Share</span></span>
<span data-ttu-id="1c376-149">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1c376-150">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="1c376-151">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="1c376-152">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-152">This object contains the storage context.</span></span>
<span data-ttu-id="1c376-153">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1c376-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c376-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1c376-154">-ShareName</span></span>
<span data-ttu-id="1c376-155">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="1c376-156">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="1c376-157">-확인</span><span class="sxs-lookup"><span data-stu-id="1c376-157">-Confirm</span></span>
<span data-ttu-id="1c376-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c376-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c376-159">-WhatIf</span></span>
<span data-ttu-id="1c376-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c376-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c376-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c376-162">CommonParameters</span></span>
<span data-ttu-id="1c376-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c376-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c376-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c376-165">입력</span><span class="sxs-lookup"><span data-stu-id="1c376-165">INPUTS</span></span>

### <span data-ttu-id="1c376-166">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="1c376-166">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="1c376-167">매개 변수: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c376-167">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="1c376-168">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="1c376-168">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="1c376-169">매개 변수: Directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c376-169">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="1c376-170">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-170">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="1c376-171">매개 변수: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c376-171">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="1c376-172">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c376-172">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c376-173">출력</span><span class="sxs-lookup"><span data-stu-id="1c376-173">OUTPUTS</span></span>

### <span data-ttu-id="1c376-174">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c376-174">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="1c376-175">상속자</span><span class="sxs-lookup"><span data-stu-id="1c376-175">NOTES</span></span>

## <span data-ttu-id="1c376-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c376-176">RELATED LINKS</span></span>

[<span data-ttu-id="1c376-177">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="1c376-177">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="1c376-178">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="1c376-178">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="1c376-179">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c376-179">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
