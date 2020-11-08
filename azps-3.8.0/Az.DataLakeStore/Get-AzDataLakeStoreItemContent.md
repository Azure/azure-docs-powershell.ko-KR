---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033952"
---
# <span data-ttu-id="1a705-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="1a705-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="1a705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a705-102">SYNOPSIS</span></span>
<span data-ttu-id="1a705-103">Data Lake Store에서 파일의 내용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="1a705-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a705-104">SYNTAX</span></span>

### <span data-ttu-id="1a705-105">PreviewFileContent (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a705-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a705-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="1a705-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a705-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="1a705-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a705-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1a705-108">DESCRIPTION</span></span>
<span data-ttu-id="1a705-109">**AzDataLakeStoreItemContent** Cmdlet은 Data Lake store에서 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="1a705-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1a705-110">EXAMPLES</span></span>

### <span data-ttu-id="1a705-111">예제 1: 파일 내용 가져오기</span><span class="sxs-lookup"><span data-stu-id="1a705-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="1a705-112">이 명령은 ContosoADL account의 파일 MyFile.txt 내용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="1a705-113">예제 2: 파일의 처음 두 행 가져오기</span><span class="sxs-lookup"><span data-stu-id="1a705-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="1a705-114">이 명령은 ContosoADL account의 파일 MyFile.txt에서 처음 두 줄로 구분 된 새 행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="1a705-115">변수</span><span class="sxs-lookup"><span data-stu-id="1a705-115">PARAMETERS</span></span>

### <span data-ttu-id="1a705-116">-계정</span><span class="sxs-lookup"><span data-stu-id="1a705-116">-Account</span></span>
<span data-ttu-id="1a705-117">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1a705-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a705-118">-DefaultProfile</span></span>
<span data-ttu-id="1a705-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a705-120">-인코딩</span><span class="sxs-lookup"><span data-stu-id="1a705-120">-Encoding</span></span>
<span data-ttu-id="1a705-121">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1a705-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a705-123">없는</span><span class="sxs-lookup"><span data-stu-id="1a705-123">Unknown</span></span>
- <span data-ttu-id="1a705-124">이름</span><span class="sxs-lookup"><span data-stu-id="1a705-124">String</span></span>
- <span data-ttu-id="1a705-125">유</span><span class="sxs-lookup"><span data-stu-id="1a705-125">Unicode</span></span>
- <span data-ttu-id="1a705-126">바이트만</span><span class="sxs-lookup"><span data-stu-id="1a705-126">Byte</span></span>
- <span data-ttu-id="1a705-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1a705-127">BigEndianUnicode</span></span>
- <span data-ttu-id="1a705-128">F</span><span class="sxs-lookup"><span data-stu-id="1a705-128">UTF8</span></span>
- <span data-ttu-id="1a705-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="1a705-129">UTF7</span></span>
- <span data-ttu-id="1a705-130">이외의</span><span class="sxs-lookup"><span data-stu-id="1a705-130">Ascii</span></span>
- <span data-ttu-id="1a705-131">기본값</span><span class="sxs-lookup"><span data-stu-id="1a705-131">Default</span></span>
- <span data-ttu-id="1a705-132">이중</span><span class="sxs-lookup"><span data-stu-id="1a705-132">Oem</span></span>
- <span data-ttu-id="1a705-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1a705-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a705-134">-Force</span><span class="sxs-lookup"><span data-stu-id="1a705-134">-Force</span></span>
<span data-ttu-id="1a705-135">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a705-136">-머리</span><span class="sxs-lookup"><span data-stu-id="1a705-136">-Head</span></span>
<span data-ttu-id="1a705-137">미리 볼 파일의 시작 부분에서 행 (새 줄 바꿈)의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="1a705-138">데이터의 첫 번째 4mb에서 새 줄이 발견 되지 않으면 해당 데이터만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="1a705-139">-길이</span><span class="sxs-lookup"><span data-stu-id="1a705-139">-Length</span></span>
<span data-ttu-id="1a705-140">가져올 콘텐츠의 길이 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="1a705-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="1a705-141">-Offset</span></span>
<span data-ttu-id="1a705-142">콘텐츠를 가져오기 전에 파일에서 건너뛸 바이트 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="1a705-143">-Path</span><span class="sxs-lookup"><span data-stu-id="1a705-143">-Path</span></span>
<span data-ttu-id="1a705-144">루트 디렉터리 (/)로 시작 하는 파일의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1a705-145">-꼬리</span><span class="sxs-lookup"><span data-stu-id="1a705-145">-Tail</span></span>
<span data-ttu-id="1a705-146">미리 볼 파일의 끝에 있는 행의 수 (새 줄 바꿈)입니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="1a705-147">데이터의 첫 번째 4mb에서 새 줄이 발견 되지 않으면 해당 데이터만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="1a705-148">-확인</span><span class="sxs-lookup"><span data-stu-id="1a705-148">-Confirm</span></span>
<span data-ttu-id="1a705-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a705-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a705-150">-WhatIf</span></span>
<span data-ttu-id="1a705-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a705-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a705-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a705-153">CommonParameters</span></span>
<span data-ttu-id="1a705-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a705-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a705-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a705-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a705-156">입력</span><span class="sxs-lookup"><span data-stu-id="1a705-156">INPUTS</span></span>

### <span data-ttu-id="1a705-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a705-157">System.String</span></span>

### <span data-ttu-id="1a705-158">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="1a705-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1a705-159">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="1a705-159">System.Int32</span></span>

### <span data-ttu-id="1a705-160">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="1a705-160">System.Int64</span></span>

### <span data-ttu-id="1a705-161">시스템. 텍스트 인코딩</span><span class="sxs-lookup"><span data-stu-id="1a705-161">System.Text.Encoding</span></span>

### <span data-ttu-id="1a705-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a705-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a705-163">출력</span><span class="sxs-lookup"><span data-stu-id="1a705-163">OUTPUTS</span></span>

### <span data-ttu-id="1a705-164">시스템 바이트</span><span class="sxs-lookup"><span data-stu-id="1a705-164">System.Byte</span></span>

### <span data-ttu-id="1a705-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a705-165">System.String</span></span>

## <span data-ttu-id="1a705-166">상속자</span><span class="sxs-lookup"><span data-stu-id="1a705-166">NOTES</span></span>

## <span data-ttu-id="1a705-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a705-167">RELATED LINKS</span></span>
