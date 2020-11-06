---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: ed931444940b86c04e027eb88da9266c7af20206
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532030"
---
# <span data-ttu-id="6c4f0-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6c4f0-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="6c4f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4f0-103">Data Lake Store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c4f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c4f0-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c4f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6c4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="6c4f0-106">**Add-AzureRmDataLakeStoreItemContent** Cmdlet은 Azure Data Lake store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="6c4f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6c4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="6c4f0-108">예제 1: 파일에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="6c4f0-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="6c4f0-109">이 명령은 파일 myFile.txt에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="6c4f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="6c4f0-110">PARAMETERS</span></span>

### <span data-ttu-id="6c4f0-111">-계정</span><span class="sxs-lookup"><span data-stu-id="6c4f0-111">-Account</span></span>
<span data-ttu-id="6c4f0-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6c4f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4f0-113">-DefaultProfile</span></span>
<span data-ttu-id="6c4f0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6c4f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c4f0-115">-인코딩</span><span class="sxs-lookup"><span data-stu-id="6c4f0-115">-Encoding</span></span>
<span data-ttu-id="6c4f0-116">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="6c4f0-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c4f0-118">없는</span><span class="sxs-lookup"><span data-stu-id="6c4f0-118">Unknown</span></span>
- <span data-ttu-id="6c4f0-119">이름</span><span class="sxs-lookup"><span data-stu-id="6c4f0-119">String</span></span>
- <span data-ttu-id="6c4f0-120">유</span><span class="sxs-lookup"><span data-stu-id="6c4f0-120">Unicode</span></span>
- <span data-ttu-id="6c4f0-121">바이트만</span><span class="sxs-lookup"><span data-stu-id="6c4f0-121">Byte</span></span>
- <span data-ttu-id="6c4f0-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="6c4f0-122">BigEndianUnicode</span></span>
- <span data-ttu-id="6c4f0-123">F</span><span class="sxs-lookup"><span data-stu-id="6c4f0-123">UTF8</span></span>
- <span data-ttu-id="6c4f0-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="6c4f0-124">UTF7</span></span>
- <span data-ttu-id="6c4f0-125">이외의</span><span class="sxs-lookup"><span data-stu-id="6c4f0-125">Ascii</span></span>
- <span data-ttu-id="6c4f0-126">기본값</span><span class="sxs-lookup"><span data-stu-id="6c4f0-126">Default</span></span>
- <span data-ttu-id="6c4f0-127">이중</span><span class="sxs-lookup"><span data-stu-id="6c4f0-127">Oem</span></span>
- <span data-ttu-id="6c4f0-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="6c4f0-128">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4f0-129">-Path</span><span class="sxs-lookup"><span data-stu-id="6c4f0-129">-Path</span></span>
<span data-ttu-id="6c4f0-130">루트 디렉터리 (/)로 시작 하 여 수정할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6c4f0-131">-값</span><span class="sxs-lookup"><span data-stu-id="6c4f0-131">-Value</span></span>
<span data-ttu-id="6c4f0-132">항목에 추가할 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4f0-133">CommonParameters</span></span>
<span data-ttu-id="6c4f0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4f0-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c4f0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4f0-136">입력</span><span class="sxs-lookup"><span data-stu-id="6c4f0-136">INPUTS</span></span>

### <span data-ttu-id="6c4f0-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6c4f0-137">System.String</span></span>

### <span data-ttu-id="6c4f0-138">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6c4f0-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="6c4f0-139">System.Object</span></span>

### <span data-ttu-id="6c4f0-140">DataLakeStore. FileSystemCmdletProviderEncoding/.</span><span class="sxs-lookup"><span data-stu-id="6c4f0-140">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

## <span data-ttu-id="6c4f0-141">출력</span><span class="sxs-lookup"><span data-stu-id="6c4f0-141">OUTPUTS</span></span>

### <span data-ttu-id="6c4f0-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6c4f0-142">System.Boolean</span></span>

## <span data-ttu-id="6c4f0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="6c4f0-143">NOTES</span></span>

## <span data-ttu-id="6c4f0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c4f0-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c4f0-145">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6c4f0-145">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


