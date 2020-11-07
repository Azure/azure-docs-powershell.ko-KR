---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535188"
---
# <span data-ttu-id="105b0-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="105b0-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="105b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105b0-102">SYNOPSIS</span></span>
<span data-ttu-id="105b0-103">Data Lake Store에서 파일의 내용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="105b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="105b0-104">SYNTAX</span></span>

### <span data-ttu-id="105b0-105">PreviewFileContent (기본값)</span><span class="sxs-lookup"><span data-stu-id="105b0-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="105b0-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="105b0-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="105b0-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="105b0-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="105b0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="105b0-108">DESCRIPTION</span></span>
<span data-ttu-id="105b0-109">**AzureRmDataLakeStoreItemContent** Cmdlet은 Data Lake store에서 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="105b0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="105b0-110">EXAMPLES</span></span>

### <span data-ttu-id="105b0-111">예제 1: 파일 내용 가져오기</span><span class="sxs-lookup"><span data-stu-id="105b0-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="105b0-112">이 명령은 ContosoADL account의 파일 MyFile.txt 내용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="105b0-113">예제 2: 파일의 처음 두 행 가져오기</span><span class="sxs-lookup"><span data-stu-id="105b0-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="105b0-114">이 명령은 ContosoADL account의 파일 MyFile.txt에서 처음 두 줄로 구분 된 새 행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="105b0-115">변수</span><span class="sxs-lookup"><span data-stu-id="105b0-115">PARAMETERS</span></span>

### <span data-ttu-id="105b0-116">-계정</span><span class="sxs-lookup"><span data-stu-id="105b0-116">-Account</span></span>
<span data-ttu-id="105b0-117">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105b0-118">-DefaultProfile</span></span>
<span data-ttu-id="105b0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="105b0-120">-인코딩</span><span class="sxs-lookup"><span data-stu-id="105b0-120">-Encoding</span></span>
<span data-ttu-id="105b0-121">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="105b0-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="105b0-123">없는</span><span class="sxs-lookup"><span data-stu-id="105b0-123">Unknown</span></span>
- <span data-ttu-id="105b0-124">이름</span><span class="sxs-lookup"><span data-stu-id="105b0-124">String</span></span>
- <span data-ttu-id="105b0-125">유</span><span class="sxs-lookup"><span data-stu-id="105b0-125">Unicode</span></span>
- <span data-ttu-id="105b0-126">바이트만</span><span class="sxs-lookup"><span data-stu-id="105b0-126">Byte</span></span>
- <span data-ttu-id="105b0-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="105b0-127">BigEndianUnicode</span></span>
- <span data-ttu-id="105b0-128">F</span><span class="sxs-lookup"><span data-stu-id="105b0-128">UTF8</span></span>
- <span data-ttu-id="105b0-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="105b0-129">UTF7</span></span>
- <span data-ttu-id="105b0-130">이외의</span><span class="sxs-lookup"><span data-stu-id="105b0-130">Ascii</span></span>
- <span data-ttu-id="105b0-131">기본값</span><span class="sxs-lookup"><span data-stu-id="105b0-131">Default</span></span>
- <span data-ttu-id="105b0-132">이중</span><span class="sxs-lookup"><span data-stu-id="105b0-132">Oem</span></span>
- <span data-ttu-id="105b0-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="105b0-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-134">-Force</span><span class="sxs-lookup"><span data-stu-id="105b0-134">-Force</span></span>
<span data-ttu-id="105b0-135">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-136">-머리</span><span class="sxs-lookup"><span data-stu-id="105b0-136">-Head</span></span>
<span data-ttu-id="105b0-137">미리 볼 파일의 시작 부분에서 행 (새 줄 바꿈)의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="105b0-138">데이터의 첫 번째 4mb에서 새 줄이 발견 되지 않으면 해당 데이터만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-139">-길이</span><span class="sxs-lookup"><span data-stu-id="105b0-139">-Length</span></span>
<span data-ttu-id="105b0-140">가져올 콘텐츠의 길이 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="105b0-141">-Offset</span></span>
<span data-ttu-id="105b0-142">콘텐츠를 가져오기 전에 파일에서 건너뛸 바이트 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-143">-Path</span><span class="sxs-lookup"><span data-stu-id="105b0-143">-Path</span></span>
<span data-ttu-id="105b0-144">루트 디렉터리 (/)로 시작 하는 파일의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-145">-꼬리</span><span class="sxs-lookup"><span data-stu-id="105b0-145">-Tail</span></span>
<span data-ttu-id="105b0-146">미리 볼 파일의 끝에 있는 행의 수 (새 줄 바꿈)입니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="105b0-147">데이터의 첫 번째 4mb에서 새 줄이 발견 되지 않으면 해당 데이터만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="105b0-148">-확인</span><span class="sxs-lookup"><span data-stu-id="105b0-148">-Confirm</span></span>
<span data-ttu-id="105b0-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="105b0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="105b0-150">-WhatIf</span></span>
<span data-ttu-id="105b0-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="105b0-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="105b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105b0-153">CommonParameters</span></span>
<span data-ttu-id="105b0-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105b0-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105b0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105b0-156">입력</span><span class="sxs-lookup"><span data-stu-id="105b0-156">INPUTS</span></span>

### <span data-ttu-id="105b0-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="105b0-157">System.String</span></span>

### <span data-ttu-id="105b0-158">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="105b0-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="105b0-159">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="105b0-159">System.Int32</span></span>

### <span data-ttu-id="105b0-160">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="105b0-160">System.Int64</span></span>

### <span data-ttu-id="105b0-161">DataLakeStore. FileSystemCmdletProviderEncoding/.</span><span class="sxs-lookup"><span data-stu-id="105b0-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="105b0-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="105b0-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="105b0-163">출력</span><span class="sxs-lookup"><span data-stu-id="105b0-163">OUTPUTS</span></span>

### <span data-ttu-id="105b0-164">시스템 바이트</span><span class="sxs-lookup"><span data-stu-id="105b0-164">System.Byte</span></span>
<span data-ttu-id="105b0-165">검색 된 파일 콘텐츠의 바이트 스트림 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="105b0-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="105b0-166">System.String</span></span>
<span data-ttu-id="105b0-167">검색 한 파일 콘텐츠의 문자열 표현 (지정 된 인코딩)입니다.</span><span class="sxs-lookup"><span data-stu-id="105b0-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="105b0-168">상속자</span><span class="sxs-lookup"><span data-stu-id="105b0-168">NOTES</span></span>

## <span data-ttu-id="105b0-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="105b0-169">RELATED LINKS</span></span>