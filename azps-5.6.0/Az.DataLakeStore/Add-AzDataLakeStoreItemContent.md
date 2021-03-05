---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994392"
---
# <span data-ttu-id="5e594-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5e594-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="5e594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e594-102">SYNOPSIS</span></span>
<span data-ttu-id="5e594-103">Data Lake Store의 항목에 콘텐츠를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="5e594-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e594-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e594-105">설명</span><span class="sxs-lookup"><span data-stu-id="5e594-105">DESCRIPTION</span></span>
<span data-ttu-id="5e594-106">**Add-AzDataLakeStoreItemContent** cmdlet은 Azure Data Lake Store의 항목에 콘텐츠를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="5e594-107">예제</span><span class="sxs-lookup"><span data-stu-id="5e594-107">EXAMPLES</span></span>

### <span data-ttu-id="5e594-108">예제 1: 파일에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="5e594-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="5e594-109">이 명령은 파일에 콘텐츠를 myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="5e594-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="5e594-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5e594-110">PARAMETERS</span></span>

### <span data-ttu-id="5e594-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5e594-111">-Account</span></span>
<span data-ttu-id="5e594-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5e594-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e594-113">-DefaultProfile</span></span>
<span data-ttu-id="5e594-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5e594-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e594-115">-인코딩</span><span class="sxs-lookup"><span data-stu-id="5e594-115">-Encoding</span></span>
<span data-ttu-id="5e594-116">만들 항목에 대한 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="5e594-117">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e594-118">알 수 없음</span><span class="sxs-lookup"><span data-stu-id="5e594-118">Unknown</span></span>
- <span data-ttu-id="5e594-119">문자열</span><span class="sxs-lookup"><span data-stu-id="5e594-119">String</span></span>
- <span data-ttu-id="5e594-120">유니코드</span><span class="sxs-lookup"><span data-stu-id="5e594-120">Unicode</span></span>
- <span data-ttu-id="5e594-121">Byte</span><span class="sxs-lookup"><span data-stu-id="5e594-121">Byte</span></span>
- <span data-ttu-id="5e594-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="5e594-122">BigEndianUnicode</span></span>
- <span data-ttu-id="5e594-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="5e594-123">UTF8</span></span>
- <span data-ttu-id="5e594-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="5e594-124">UTF7</span></span>
- <span data-ttu-id="5e594-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="5e594-125">Ascii</span></span>
- <span data-ttu-id="5e594-126">기본값</span><span class="sxs-lookup"><span data-stu-id="5e594-126">Default</span></span>
- <span data-ttu-id="5e594-127">Oem</span><span class="sxs-lookup"><span data-stu-id="5e594-127">Oem</span></span>
- <span data-ttu-id="5e594-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="5e594-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="5e594-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5e594-129">-Path</span></span>
<span data-ttu-id="5e594-130">루트 디렉터리(/)로 시작하여 수정할 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5e594-131">-Value</span><span class="sxs-lookup"><span data-stu-id="5e594-131">-Value</span></span>
<span data-ttu-id="5e594-132">항목에 추가할 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="5e594-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e594-133">CommonParameters</span></span>
<span data-ttu-id="5e594-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e594-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e594-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e594-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e594-136">입력</span><span class="sxs-lookup"><span data-stu-id="5e594-136">INPUTS</span></span>

### <span data-ttu-id="5e594-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5e594-137">System.String</span></span>

### <span data-ttu-id="5e594-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5e594-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5e594-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="5e594-139">System.Object</span></span>

### <span data-ttu-id="5e594-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="5e594-140">System.Text.Encoding</span></span>

## <span data-ttu-id="5e594-141">출력</span><span class="sxs-lookup"><span data-stu-id="5e594-141">OUTPUTS</span></span>

### <span data-ttu-id="5e594-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e594-142">System.Boolean</span></span>

## <span data-ttu-id="5e594-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e594-143">NOTES</span></span>

## <span data-ttu-id="5e594-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e594-144">RELATED LINKS</span></span>

[<span data-ttu-id="5e594-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5e594-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


