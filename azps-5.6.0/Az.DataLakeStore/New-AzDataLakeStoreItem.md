---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991424"
---
# <span data-ttu-id="bcb84-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="bcb84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb84-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb84-103">Data Lake Store에서 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bcb84-104">구문</span><span class="sxs-lookup"><span data-stu-id="bcb84-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb84-105">설명</span><span class="sxs-lookup"><span data-stu-id="bcb84-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb84-106">**New-AzDataLakeStoreItem** cmdlet은 Data Lake Store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bcb84-107">예제</span><span class="sxs-lookup"><span data-stu-id="bcb84-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb84-108">예제 1: 새 파일 및 새 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="bcb84-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="bcb84-109">첫 번째 명령은 지정된 계정에 NewFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="bcb84-110">두 번째 명령은 루트 폴더에 NewFolder 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="bcb84-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bcb84-111">PARAMETERS</span></span>

### <span data-ttu-id="bcb84-112">-Account</span><span class="sxs-lookup"><span data-stu-id="bcb84-112">-Account</span></span>
<span data-ttu-id="bcb84-113">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bcb84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb84-114">-DefaultProfile</span></span>
<span data-ttu-id="bcb84-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb84-116">-인코딩</span><span class="sxs-lookup"><span data-stu-id="bcb84-116">-Encoding</span></span>
<span data-ttu-id="bcb84-117">만들 항목에 대한 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="bcb84-118">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcb84-119">알 수 없음</span><span class="sxs-lookup"><span data-stu-id="bcb84-119">Unknown</span></span>
- <span data-ttu-id="bcb84-120">문자열</span><span class="sxs-lookup"><span data-stu-id="bcb84-120">String</span></span>
- <span data-ttu-id="bcb84-121">유니코드</span><span class="sxs-lookup"><span data-stu-id="bcb84-121">Unicode</span></span>
- <span data-ttu-id="bcb84-122">Byte</span><span class="sxs-lookup"><span data-stu-id="bcb84-122">Byte</span></span>
- <span data-ttu-id="bcb84-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="bcb84-123">BigEndianUnicode</span></span>
- <span data-ttu-id="bcb84-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="bcb84-124">UTF8</span></span>
- <span data-ttu-id="bcb84-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="bcb84-125">UTF7</span></span>
- <span data-ttu-id="bcb84-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="bcb84-126">Ascii</span></span>
- <span data-ttu-id="bcb84-127">기본값</span><span class="sxs-lookup"><span data-stu-id="bcb84-127">Default</span></span>
- <span data-ttu-id="bcb84-128">Oem</span><span class="sxs-lookup"><span data-stu-id="bcb84-128">Oem</span></span>
- <span data-ttu-id="bcb84-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="bcb84-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="bcb84-130">-폴더</span><span class="sxs-lookup"><span data-stu-id="bcb84-130">-Folder</span></span>
<span data-ttu-id="bcb84-131">이 작업은 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="bcb84-132">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb84-132">-Force</span></span>
<span data-ttu-id="bcb84-133">이 작업이 이미 있는 경우 대상 항목을 덮어써도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="bcb84-134">-Path</span><span class="sxs-lookup"><span data-stu-id="bcb84-134">-Path</span></span>
<span data-ttu-id="bcb84-135">루트 디렉터리(/)로 시작하여 만들 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="bcb84-136">-Value</span><span class="sxs-lookup"><span data-stu-id="bcb84-136">-Value</span></span>
<span data-ttu-id="bcb84-137">만들 항목에 추가할 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="bcb84-138">-확인</span><span class="sxs-lookup"><span data-stu-id="bcb84-138">-Confirm</span></span>
<span data-ttu-id="bcb84-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb84-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb84-140">-WhatIf</span></span>
<span data-ttu-id="bcb84-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb84-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb84-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb84-143">CommonParameters</span></span>
<span data-ttu-id="bcb84-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcb84-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb84-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bcb84-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb84-146">입력</span><span class="sxs-lookup"><span data-stu-id="bcb84-146">INPUTS</span></span>

### <span data-ttu-id="bcb84-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb84-147">System.String</span></span>

### <span data-ttu-id="bcb84-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bcb84-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bcb84-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="bcb84-149">System.Object</span></span>

### <span data-ttu-id="bcb84-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="bcb84-150">System.Text.Encoding</span></span>

### <span data-ttu-id="bcb84-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bcb84-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bcb84-152">출력</span><span class="sxs-lookup"><span data-stu-id="bcb84-152">OUTPUTS</span></span>

### <span data-ttu-id="bcb84-153">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb84-153">System.String</span></span>

## <span data-ttu-id="bcb84-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcb84-154">NOTES</span></span>

## <span data-ttu-id="bcb84-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcb84-155">RELATED LINKS</span></span>

[<span data-ttu-id="bcb84-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="bcb84-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="bcb84-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="bcb84-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="bcb84-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="bcb84-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bcb84-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


