---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526844"
---
# <span data-ttu-id="95b11-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="95b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95b11-102">SYNOPSIS</span></span>
<span data-ttu-id="95b11-103">Data Lake Store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95b11-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95b11-105">DESCRIPTION</span></span>
<span data-ttu-id="95b11-106">**AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에 새 파일 또는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95b11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95b11-107">EXAMPLES</span></span>

### <span data-ttu-id="95b11-108">예제 1: 새 파일 및 새 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="95b11-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="95b11-109">첫 번째 명령은 지정 된 계정에 대 한 NewFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="95b11-110">두 번째 명령은 루트 폴더에 NewFolder 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="95b11-111">변수</span><span class="sxs-lookup"><span data-stu-id="95b11-111">PARAMETERS</span></span>

### <span data-ttu-id="95b11-112">-계정</span><span class="sxs-lookup"><span data-stu-id="95b11-112">-Account</span></span>
<span data-ttu-id="95b11-113">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b11-114">-DefaultProfile</span></span>
<span data-ttu-id="95b11-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b11-116">-인코딩</span><span class="sxs-lookup"><span data-stu-id="95b11-116">-Encoding</span></span>
<span data-ttu-id="95b11-117">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="95b11-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95b11-119">없는</span><span class="sxs-lookup"><span data-stu-id="95b11-119">Unknown</span></span>
- <span data-ttu-id="95b11-120">이름</span><span class="sxs-lookup"><span data-stu-id="95b11-120">String</span></span>
- <span data-ttu-id="95b11-121">유</span><span class="sxs-lookup"><span data-stu-id="95b11-121">Unicode</span></span>
- <span data-ttu-id="95b11-122">바이트만</span><span class="sxs-lookup"><span data-stu-id="95b11-122">Byte</span></span>
- <span data-ttu-id="95b11-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="95b11-123">BigEndianUnicode</span></span>
- <span data-ttu-id="95b11-124">F</span><span class="sxs-lookup"><span data-stu-id="95b11-124">UTF8</span></span>
- <span data-ttu-id="95b11-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="95b11-125">UTF7</span></span>
- <span data-ttu-id="95b11-126">이외의</span><span class="sxs-lookup"><span data-stu-id="95b11-126">Ascii</span></span>
- <span data-ttu-id="95b11-127">기본값</span><span class="sxs-lookup"><span data-stu-id="95b11-127">Default</span></span>
- <span data-ttu-id="95b11-128">이중</span><span class="sxs-lookup"><span data-stu-id="95b11-128">Oem</span></span>
- <span data-ttu-id="95b11-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="95b11-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-130">-폴더</span><span class="sxs-lookup"><span data-stu-id="95b11-130">-Folder</span></span>
<span data-ttu-id="95b11-131">이 작업을 통해 폴더가 생성 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-132">-Force</span><span class="sxs-lookup"><span data-stu-id="95b11-132">-Force</span></span>
<span data-ttu-id="95b11-133">이 작업이 이미 있는 경우 대상 항목을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-134">-Path</span><span class="sxs-lookup"><span data-stu-id="95b11-134">-Path</span></span>
<span data-ttu-id="95b11-135">루트 디렉터리 (/)로 시작 하 여 만들 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-136">-값</span><span class="sxs-lookup"><span data-stu-id="95b11-136">-Value</span></span>
<span data-ttu-id="95b11-137">사용자가 만든 항목에 추가할 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-138">-확인</span><span class="sxs-lookup"><span data-stu-id="95b11-138">-Confirm</span></span>
<span data-ttu-id="95b11-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b11-140">-WhatIf</span></span>
<span data-ttu-id="95b11-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95b11-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95b11-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b11-143">CommonParameters</span></span>
<span data-ttu-id="95b11-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b11-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b11-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b11-146">입력</span><span class="sxs-lookup"><span data-stu-id="95b11-146">INPUTS</span></span>

### <span data-ttu-id="95b11-147">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="95b11-147">Object</span></span>
<span data-ttu-id="95b11-148">' Value ' 매개 변수는 파이프라인에서 ' Object ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="95b11-149">출력</span><span class="sxs-lookup"><span data-stu-id="95b11-149">OUTPUTS</span></span>

### <span data-ttu-id="95b11-150">이름</span><span class="sxs-lookup"><span data-stu-id="95b11-150">string</span></span>
<span data-ttu-id="95b11-151">생성 된 파일 또는 폴더의 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="95b11-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="95b11-152">상속자</span><span class="sxs-lookup"><span data-stu-id="95b11-152">NOTES</span></span>

## <span data-ttu-id="95b11-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95b11-153">RELATED LINKS</span></span>

[<span data-ttu-id="95b11-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95b11-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95b11-156">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95b11-157">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95b11-158">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95b11-159">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95b11-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


