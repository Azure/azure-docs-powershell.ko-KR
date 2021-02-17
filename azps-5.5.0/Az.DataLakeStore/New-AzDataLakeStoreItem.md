---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186164"
---
# <span data-ttu-id="acb0e-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="acb0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="acb0e-103">Data Lake Store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="acb0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="acb0e-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acb0e-105">설명</span><span class="sxs-lookup"><span data-stu-id="acb0e-105">DESCRIPTION</span></span>
<span data-ttu-id="acb0e-106">**New-AzDataLakeStoreItem** cmdlet은 Data Lake Store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="acb0e-107">예제</span><span class="sxs-lookup"><span data-stu-id="acb0e-107">EXAMPLES</span></span>

### <span data-ttu-id="acb0e-108">예제 1: 새 파일 및 새 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="acb0e-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="acb0e-109">첫 번째 명령은 지정된 계정에 NewFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="acb0e-110">두 번째 명령은 루트 폴더에 NewFolder 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="acb0e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acb0e-111">PARAMETERS</span></span>

### <span data-ttu-id="acb0e-112">-Account</span><span class="sxs-lookup"><span data-stu-id="acb0e-112">-Account</span></span>
<span data-ttu-id="acb0e-113">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="acb0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb0e-114">-DefaultProfile</span></span>
<span data-ttu-id="acb0e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb0e-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="acb0e-116">-Encoding</span></span>
<span data-ttu-id="acb0e-117">만들 항목에 대한 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="acb0e-118">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="acb0e-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="acb0e-119">알 수 없음</span><span class="sxs-lookup"><span data-stu-id="acb0e-119">Unknown</span></span>
- <span data-ttu-id="acb0e-120">문자열</span><span class="sxs-lookup"><span data-stu-id="acb0e-120">String</span></span>
- <span data-ttu-id="acb0e-121">유니코드</span><span class="sxs-lookup"><span data-stu-id="acb0e-121">Unicode</span></span>
- <span data-ttu-id="acb0e-122">Byte</span><span class="sxs-lookup"><span data-stu-id="acb0e-122">Byte</span></span>
- <span data-ttu-id="acb0e-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="acb0e-123">BigEndianUnicode</span></span>
- <span data-ttu-id="acb0e-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="acb0e-124">UTF8</span></span>
- <span data-ttu-id="acb0e-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="acb0e-125">UTF7</span></span>
- <span data-ttu-id="acb0e-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="acb0e-126">Ascii</span></span>
- <span data-ttu-id="acb0e-127">기본값</span><span class="sxs-lookup"><span data-stu-id="acb0e-127">Default</span></span>
- <span data-ttu-id="acb0e-128">Oem</span><span class="sxs-lookup"><span data-stu-id="acb0e-128">Oem</span></span>
- <span data-ttu-id="acb0e-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="acb0e-129">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb0e-130">-Folder</span><span class="sxs-lookup"><span data-stu-id="acb0e-130">-Folder</span></span>
<span data-ttu-id="acb0e-131">이 작업이 폴더를 만들 것 을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb0e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="acb0e-132">-Force</span></span>
<span data-ttu-id="acb0e-133">이 작업이 이미 있는 경우 대상 항목을 덮어써도 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb0e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="acb0e-134">-Path</span></span>
<span data-ttu-id="acb0e-135">루트 디렉터리(/)로 시작하여 만들 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="acb0e-136">-Value</span><span class="sxs-lookup"><span data-stu-id="acb0e-136">-Value</span></span>
<span data-ttu-id="acb0e-137">만들 항목에 추가할 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acb0e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acb0e-138">-Confirm</span></span>
<span data-ttu-id="acb0e-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acb0e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb0e-140">-WhatIf</span></span>
<span data-ttu-id="acb0e-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="acb0e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acb0e-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acb0e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb0e-143">CommonParameters</span></span>
<span data-ttu-id="acb0e-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="acb0e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb0e-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="acb0e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb0e-146">입력</span><span class="sxs-lookup"><span data-stu-id="acb0e-146">INPUTS</span></span>

### <span data-ttu-id="acb0e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="acb0e-147">System.String</span></span>

### <span data-ttu-id="acb0e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="acb0e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="acb0e-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="acb0e-149">System.Object</span></span>

### <span data-ttu-id="acb0e-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="acb0e-150">System.Text.Encoding</span></span>

### <span data-ttu-id="acb0e-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="acb0e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="acb0e-152">출력</span><span class="sxs-lookup"><span data-stu-id="acb0e-152">OUTPUTS</span></span>

### <span data-ttu-id="acb0e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="acb0e-153">System.String</span></span>

## <span data-ttu-id="acb0e-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="acb0e-154">NOTES</span></span>

## <span data-ttu-id="acb0e-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acb0e-155">RELATED LINKS</span></span>

[<span data-ttu-id="acb0e-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="acb0e-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="acb0e-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="acb0e-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="acb0e-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="acb0e-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="acb0e-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


