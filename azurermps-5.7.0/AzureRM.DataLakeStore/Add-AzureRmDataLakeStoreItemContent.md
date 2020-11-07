---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: f272d7c57a1543f916d828d6324dd23f5780ccad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702656"
---
# <span data-ttu-id="a30f2-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a30f2-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="a30f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a30f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a30f2-103">Data Lake Store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a30f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a30f2-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a30f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a30f2-105">DESCRIPTION</span></span>
<span data-ttu-id="a30f2-106">**Add-AzureRmDataLakeStoreItemContent** Cmdlet은 Azure Data Lake store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="a30f2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a30f2-107">EXAMPLES</span></span>

### <span data-ttu-id="a30f2-108">예제 1: 파일에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="a30f2-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="a30f2-109">이 명령은 파일 myFile.txt에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="a30f2-110">변수</span><span class="sxs-lookup"><span data-stu-id="a30f2-110">PARAMETERS</span></span>

### <span data-ttu-id="a30f2-111">-계정</span><span class="sxs-lookup"><span data-stu-id="a30f2-111">-Account</span></span>
<span data-ttu-id="a30f2-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a30f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30f2-113">-DefaultProfile</span></span>
<span data-ttu-id="a30f2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a30f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a30f2-115">-인코딩</span><span class="sxs-lookup"><span data-stu-id="a30f2-115">-Encoding</span></span>
<span data-ttu-id="a30f2-116">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a30f2-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a30f2-118">없는</span><span class="sxs-lookup"><span data-stu-id="a30f2-118">Unknown</span></span>
- <span data-ttu-id="a30f2-119">이름</span><span class="sxs-lookup"><span data-stu-id="a30f2-119">String</span></span>
- <span data-ttu-id="a30f2-120">유</span><span class="sxs-lookup"><span data-stu-id="a30f2-120">Unicode</span></span>
- <span data-ttu-id="a30f2-121">바이트만</span><span class="sxs-lookup"><span data-stu-id="a30f2-121">Byte</span></span>
- <span data-ttu-id="a30f2-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a30f2-122">BigEndianUnicode</span></span>
- <span data-ttu-id="a30f2-123">F</span><span class="sxs-lookup"><span data-stu-id="a30f2-123">UTF8</span></span>
- <span data-ttu-id="a30f2-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="a30f2-124">UTF7</span></span>
- <span data-ttu-id="a30f2-125">이외의</span><span class="sxs-lookup"><span data-stu-id="a30f2-125">Ascii</span></span>
- <span data-ttu-id="a30f2-126">기본값</span><span class="sxs-lookup"><span data-stu-id="a30f2-126">Default</span></span>
- <span data-ttu-id="a30f2-127">이중</span><span class="sxs-lookup"><span data-stu-id="a30f2-127">Oem</span></span>
- <span data-ttu-id="a30f2-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a30f2-128">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a30f2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="a30f2-129">-Path</span></span>
<span data-ttu-id="a30f2-130">루트 디렉터리 (/)로 시작 하 여 수정할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a30f2-131">-값</span><span class="sxs-lookup"><span data-stu-id="a30f2-131">-Value</span></span>
<span data-ttu-id="a30f2-132">항목에 추가할 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-132">Specifies the content to add to the item.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a30f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30f2-133">CommonParameters</span></span>
<span data-ttu-id="a30f2-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30f2-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a30f2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30f2-136">입력</span><span class="sxs-lookup"><span data-stu-id="a30f2-136">INPUTS</span></span>

### <span data-ttu-id="a30f2-137">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="a30f2-137">Object</span></span>
<span data-ttu-id="a30f2-138">' Value ' 매개 변수는 파이프라인에서 ' Object ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="a30f2-139">출력</span><span class="sxs-lookup"><span data-stu-id="a30f2-139">OUTPUTS</span></span>

### <span data-ttu-id="a30f2-140">부울</span><span class="sxs-lookup"><span data-stu-id="a30f2-140">bool</span></span>
<span data-ttu-id="a30f2-141">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a30f2-141">Returns true on success.</span></span>

## <span data-ttu-id="a30f2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a30f2-142">NOTES</span></span>

## <span data-ttu-id="a30f2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a30f2-143">RELATED LINKS</span></span>

[<span data-ttu-id="a30f2-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a30f2-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


