---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868517"
---
# <span data-ttu-id="da79e-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="da79e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da79e-102">SYNOPSIS</span></span>
<span data-ttu-id="da79e-103">Data Lake Store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da79e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da79e-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da79e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da79e-105">DESCRIPTION</span></span>
<span data-ttu-id="da79e-106">**AzDataLakeStoreItem** Cmdlet은 Data Lake store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="da79e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da79e-107">EXAMPLES</span></span>

### <span data-ttu-id="da79e-108">예제 1: 새 파일 및 새 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="da79e-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="da79e-109">첫 번째 명령은 지정 된 계정에 대 한 NewFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="da79e-110">두 번째 명령은 루트 폴더에 NewFolder 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="da79e-111">변수</span><span class="sxs-lookup"><span data-stu-id="da79e-111">PARAMETERS</span></span>

### <span data-ttu-id="da79e-112">-계정</span><span class="sxs-lookup"><span data-stu-id="da79e-112">-Account</span></span>
<span data-ttu-id="da79e-113">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="da79e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da79e-114">-DefaultProfile</span></span>
<span data-ttu-id="da79e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da79e-116">-인코딩</span><span class="sxs-lookup"><span data-stu-id="da79e-116">-Encoding</span></span>
<span data-ttu-id="da79e-117">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="da79e-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da79e-119">없는</span><span class="sxs-lookup"><span data-stu-id="da79e-119">Unknown</span></span>
- <span data-ttu-id="da79e-120">이름</span><span class="sxs-lookup"><span data-stu-id="da79e-120">String</span></span>
- <span data-ttu-id="da79e-121">유</span><span class="sxs-lookup"><span data-stu-id="da79e-121">Unicode</span></span>
- <span data-ttu-id="da79e-122">바이트만</span><span class="sxs-lookup"><span data-stu-id="da79e-122">Byte</span></span>
- <span data-ttu-id="da79e-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="da79e-123">BigEndianUnicode</span></span>
- <span data-ttu-id="da79e-124">F</span><span class="sxs-lookup"><span data-stu-id="da79e-124">UTF8</span></span>
- <span data-ttu-id="da79e-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="da79e-125">UTF7</span></span>
- <span data-ttu-id="da79e-126">이외의</span><span class="sxs-lookup"><span data-stu-id="da79e-126">Ascii</span></span>
- <span data-ttu-id="da79e-127">기본값</span><span class="sxs-lookup"><span data-stu-id="da79e-127">Default</span></span>
- <span data-ttu-id="da79e-128">이중</span><span class="sxs-lookup"><span data-stu-id="da79e-128">Oem</span></span>
- <span data-ttu-id="da79e-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="da79e-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="da79e-130">-폴더</span><span class="sxs-lookup"><span data-stu-id="da79e-130">-Folder</span></span>
<span data-ttu-id="da79e-131">이 작업을 통해 폴더가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="da79e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="da79e-132">-Force</span></span>
<span data-ttu-id="da79e-133">이 작업이 이미 있는 경우 대상 항목을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="da79e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="da79e-134">-Path</span></span>
<span data-ttu-id="da79e-135">루트 디렉터리 (/)로 시작 하 여 만들 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="da79e-136">-값</span><span class="sxs-lookup"><span data-stu-id="da79e-136">-Value</span></span>
<span data-ttu-id="da79e-137">사용자가 만든 항목에 추가할 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="da79e-138">-확인</span><span class="sxs-lookup"><span data-stu-id="da79e-138">-Confirm</span></span>
<span data-ttu-id="da79e-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da79e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da79e-140">-WhatIf</span></span>
<span data-ttu-id="da79e-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da79e-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da79e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da79e-143">CommonParameters</span></span>
<span data-ttu-id="da79e-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da79e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da79e-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da79e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da79e-146">입력</span><span class="sxs-lookup"><span data-stu-id="da79e-146">INPUTS</span></span>

### <span data-ttu-id="da79e-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da79e-147">System.String</span></span>

### <span data-ttu-id="da79e-148">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="da79e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="da79e-149">System. 개체</span><span class="sxs-lookup"><span data-stu-id="da79e-149">System.Object</span></span>

### <span data-ttu-id="da79e-150">시스템. 텍스트 인코딩</span><span class="sxs-lookup"><span data-stu-id="da79e-150">System.Text.Encoding</span></span>

### <span data-ttu-id="da79e-151">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="da79e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="da79e-152">출력</span><span class="sxs-lookup"><span data-stu-id="da79e-152">OUTPUTS</span></span>

### <span data-ttu-id="da79e-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da79e-153">System.String</span></span>

## <span data-ttu-id="da79e-154">상속자</span><span class="sxs-lookup"><span data-stu-id="da79e-154">NOTES</span></span>

## <span data-ttu-id="da79e-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da79e-155">RELATED LINKS</span></span>

[<span data-ttu-id="da79e-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="da79e-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="da79e-158">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="da79e-159">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="da79e-160">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="da79e-161">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da79e-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


