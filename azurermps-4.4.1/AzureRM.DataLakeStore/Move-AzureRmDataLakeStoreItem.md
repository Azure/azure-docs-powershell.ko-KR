---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5d975e70423e03e3ab17bbfc8631ff8e1f892cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703744"
---
# <span data-ttu-id="83bea-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="83bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83bea-102">SYNOPSIS</span></span>
<span data-ttu-id="83bea-103">Data Lake Store에서 파일 또는 폴더를 이동 하거나 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83bea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83bea-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83bea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83bea-105">DESCRIPTION</span></span>
<span data-ttu-id="83bea-106">**AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일 또는 폴더를 이동 하거나 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83bea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83bea-107">EXAMPLES</span></span>

### <span data-ttu-id="83bea-108">예제 1: 항목 이동 및 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="83bea-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="83bea-109">이 명령은 항목 File.txt의 이름을 RenamedFile.txt 변경 하 고 다른 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="83bea-110">변수</span><span class="sxs-lookup"><span data-stu-id="83bea-110">PARAMETERS</span></span>

### <span data-ttu-id="83bea-111">-계정</span><span class="sxs-lookup"><span data-stu-id="83bea-111">-Account</span></span>
<span data-ttu-id="83bea-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="83bea-113">-대상</span><span class="sxs-lookup"><span data-stu-id="83bea-113">-Destination</span></span>
<span data-ttu-id="83bea-114">루트 디렉터리 (/)로 시작 하 여 항목을 이동할 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-114">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83bea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83bea-115">-Force</span></span>
<span data-ttu-id="83bea-116">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="83bea-117">-Path</span><span class="sxs-lookup"><span data-stu-id="83bea-117">-Path</span></span>
<span data-ttu-id="83bea-118">루트 디렉터리 (/)로 시작 하 여 이동 하거나 이름을 바꿀 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-118">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="83bea-119">-확인</span><span class="sxs-lookup"><span data-stu-id="83bea-119">-Confirm</span></span>
<span data-ttu-id="83bea-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83bea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83bea-121">-WhatIf</span></span>
<span data-ttu-id="83bea-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83bea-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83bea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83bea-124">-DefaultProfile</span></span>
<span data-ttu-id="83bea-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83bea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83bea-126">CommonParameters</span></span>
<span data-ttu-id="83bea-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83bea-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83bea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83bea-129">입력</span><span class="sxs-lookup"><span data-stu-id="83bea-129">INPUTS</span></span>

## <span data-ttu-id="83bea-130">출력</span><span class="sxs-lookup"><span data-stu-id="83bea-130">OUTPUTS</span></span>

### <span data-ttu-id="83bea-131">이름</span><span class="sxs-lookup"><span data-stu-id="83bea-131">string</span></span>
<span data-ttu-id="83bea-132">이동한 파일 또는 폴더에 대 한 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="83bea-132">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="83bea-133">상속자</span><span class="sxs-lookup"><span data-stu-id="83bea-133">NOTES</span></span>

## <span data-ttu-id="83bea-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83bea-134">RELATED LINKS</span></span>

[<span data-ttu-id="83bea-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83bea-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83bea-137">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83bea-138">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83bea-139">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83bea-140">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83bea-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


