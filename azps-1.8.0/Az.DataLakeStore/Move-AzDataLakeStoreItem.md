---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868518"
---
# <span data-ttu-id="b855e-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b855e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b855e-102">SYNOPSIS</span></span>
<span data-ttu-id="b855e-103">Data Lake Store에서 파일 또는 폴더를 이동 하거나 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b855e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b855e-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b855e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b855e-105">DESCRIPTION</span></span>
<span data-ttu-id="b855e-106">**AzDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일 또는 폴더를 이동 하거나 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b855e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b855e-107">EXAMPLES</span></span>

### <span data-ttu-id="b855e-108">예제 1: 항목 이동 및 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="b855e-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="b855e-109">이 명령은 항목 File.txt의 이름을 RenamedFile.txt 변경 하 고 다른 폴더로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="b855e-110">변수</span><span class="sxs-lookup"><span data-stu-id="b855e-110">PARAMETERS</span></span>

### <span data-ttu-id="b855e-111">-계정</span><span class="sxs-lookup"><span data-stu-id="b855e-111">-Account</span></span>
<span data-ttu-id="b855e-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b855e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b855e-113">-DefaultProfile</span></span>
<span data-ttu-id="b855e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b855e-115">-대상</span><span class="sxs-lookup"><span data-stu-id="b855e-115">-Destination</span></span>
<span data-ttu-id="b855e-116">루트 디렉터리 (/)로 시작 하 여 항목을 이동할 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b855e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b855e-117">-Force</span></span>
<span data-ttu-id="b855e-118">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b855e-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b855e-119">-Path</span></span>
<span data-ttu-id="b855e-120">루트 디렉터리 (/)로 시작 하 여 이동 하거나 이름을 바꿀 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b855e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b855e-121">-Confirm</span></span>
<span data-ttu-id="b855e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b855e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b855e-123">-WhatIf</span></span>
<span data-ttu-id="b855e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b855e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b855e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b855e-126">CommonParameters</span></span>
<span data-ttu-id="b855e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b855e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b855e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b855e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b855e-129">입력</span><span class="sxs-lookup"><span data-stu-id="b855e-129">INPUTS</span></span>

### <span data-ttu-id="b855e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b855e-130">System.String</span></span>

### <span data-ttu-id="b855e-131">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="b855e-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b855e-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b855e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b855e-133">출력</span><span class="sxs-lookup"><span data-stu-id="b855e-133">OUTPUTS</span></span>

### <span data-ttu-id="b855e-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b855e-134">System.String</span></span>

## <span data-ttu-id="b855e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b855e-135">NOTES</span></span>

## <span data-ttu-id="b855e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b855e-136">RELATED LINKS</span></span>

[<span data-ttu-id="b855e-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="b855e-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b855e-139">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b855e-140">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b855e-141">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="b855e-142">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b855e-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


