---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: e5aaff4f915143e2e7695c9f650aed6fb01ba389
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196569"
---
# <span data-ttu-id="99d22-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="99d22-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="99d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d22-102">SYNOPSIS</span></span>
<span data-ttu-id="99d22-103">Data Lake Store에서 파일의 내용을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="99d22-104">구문</span><span class="sxs-lookup"><span data-stu-id="99d22-104">SYNTAX</span></span>

### <span data-ttu-id="99d22-105">PreviewFileContent(기본값)</span><span class="sxs-lookup"><span data-stu-id="99d22-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d22-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="99d22-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d22-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="99d22-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d22-108">설명</span><span class="sxs-lookup"><span data-stu-id="99d22-108">DESCRIPTION</span></span>
<span data-ttu-id="99d22-109">**Get-AzDataLakeStoreItemContent** cmdlet은 Data Lake Store에서 파일의 콘텐츠를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="99d22-110">예제</span><span class="sxs-lookup"><span data-stu-id="99d22-110">EXAMPLES</span></span>

### <span data-ttu-id="99d22-111">예제 1: 파일 내용 얻기</span><span class="sxs-lookup"><span data-stu-id="99d22-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="99d22-112">이 명령은 ContosoADL 계정에 MyFile.txt 파일의 콘텐츠를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="99d22-113">예제 2: 파일의 처음 두 행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="99d22-114">이 명령은 ContosoADL 계정의 파일 MyFile.txt 처음 두 줄로 구분된 행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="99d22-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99d22-115">PARAMETERS</span></span>

### <span data-ttu-id="99d22-116">-Account</span><span class="sxs-lookup"><span data-stu-id="99d22-116">-Account</span></span>
<span data-ttu-id="99d22-117">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="99d22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d22-118">-DefaultProfile</span></span>
<span data-ttu-id="99d22-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d22-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="99d22-120">-Encoding</span></span>
<span data-ttu-id="99d22-121">만들 항목에 대한 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="99d22-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="99d22-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99d22-123">알 수 없음</span><span class="sxs-lookup"><span data-stu-id="99d22-123">Unknown</span></span>
- <span data-ttu-id="99d22-124">문자열</span><span class="sxs-lookup"><span data-stu-id="99d22-124">String</span></span>
- <span data-ttu-id="99d22-125">유니코드</span><span class="sxs-lookup"><span data-stu-id="99d22-125">Unicode</span></span>
- <span data-ttu-id="99d22-126">Byte</span><span class="sxs-lookup"><span data-stu-id="99d22-126">Byte</span></span>
- <span data-ttu-id="99d22-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="99d22-127">BigEndianUnicode</span></span>
- <span data-ttu-id="99d22-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="99d22-128">UTF8</span></span>
- <span data-ttu-id="99d22-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="99d22-129">UTF7</span></span>
- <span data-ttu-id="99d22-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="99d22-130">Ascii</span></span>
- <span data-ttu-id="99d22-131">기본값</span><span class="sxs-lookup"><span data-stu-id="99d22-131">Default</span></span>
- <span data-ttu-id="99d22-132">Oem</span><span class="sxs-lookup"><span data-stu-id="99d22-132">Oem</span></span>
- <span data-ttu-id="99d22-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="99d22-133">BigEndianUTF32</span></span>

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

### <span data-ttu-id="99d22-134">-Force</span><span class="sxs-lookup"><span data-stu-id="99d22-134">-Force</span></span>
<span data-ttu-id="99d22-135">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99d22-136">-Head</span><span class="sxs-lookup"><span data-stu-id="99d22-136">-Head</span></span>
<span data-ttu-id="99d22-137">미리 보기할 파일의 시작부터 행 수(새 줄로 나타)입니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="99d22-138">데이터의 처음 4mb에 새 줄이 없는 경우 해당 데이터만 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="99d22-139">-Length</span><span class="sxs-lookup"><span data-stu-id="99d22-139">-Length</span></span>
<span data-ttu-id="99d22-140">얻을 콘텐츠의 길이(byte)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="99d22-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="99d22-141">-Offset</span></span>
<span data-ttu-id="99d22-142">콘텐츠를 시작하기 전에 파일에서 건너뛸 수 있는 byte 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="99d22-143">-Path</span><span class="sxs-lookup"><span data-stu-id="99d22-143">-Path</span></span>
<span data-ttu-id="99d22-144">루트 디렉터리(/)로 시작하는 파일의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="99d22-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="99d22-145">-Tail</span></span>
<span data-ttu-id="99d22-146">미리 보기할 파일의 끝에서 행 수(새 줄로 나타났습니다.)</span><span class="sxs-lookup"><span data-stu-id="99d22-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="99d22-147">데이터의 처음 4mb에 새 줄이 없는 경우 해당 데이터만 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="99d22-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99d22-148">-Confirm</span></span>
<span data-ttu-id="99d22-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d22-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d22-150">-WhatIf</span></span>
<span data-ttu-id="99d22-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99d22-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d22-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d22-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d22-153">CommonParameters</span></span>
<span data-ttu-id="99d22-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99d22-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d22-155">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99d22-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d22-156">입력</span><span class="sxs-lookup"><span data-stu-id="99d22-156">INPUTS</span></span>

### <span data-ttu-id="99d22-157">System.String</span><span class="sxs-lookup"><span data-stu-id="99d22-157">System.String</span></span>

### <span data-ttu-id="99d22-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="99d22-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="99d22-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="99d22-159">System.Int32</span></span>

### <span data-ttu-id="99d22-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="99d22-160">System.Int64</span></span>

### <span data-ttu-id="99d22-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="99d22-161">System.Text.Encoding</span></span>

### <span data-ttu-id="99d22-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99d22-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99d22-163">출력</span><span class="sxs-lookup"><span data-stu-id="99d22-163">OUTPUTS</span></span>

### <span data-ttu-id="99d22-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="99d22-164">System.Byte</span></span>

### <span data-ttu-id="99d22-165">System.String</span><span class="sxs-lookup"><span data-stu-id="99d22-165">System.String</span></span>

## <span data-ttu-id="99d22-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99d22-166">NOTES</span></span>

## <span data-ttu-id="99d22-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99d22-167">RELATED LINKS</span></span>
