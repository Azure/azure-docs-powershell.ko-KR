---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 7ff40890783edbfaf610434f0b25ad04b4b3be21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701066"
---
# <span data-ttu-id="4bedf-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="4bedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bedf-102">SYNOPSIS</span></span>
<span data-ttu-id="4bedf-103">하나 이상의 파일을 조인 하 여 Data Lake Store에 하나의 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="4bedf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bedf-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bedf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bedf-105">DESCRIPTION</span></span>
<span data-ttu-id="4bedf-106">AzDataLakeStoreItem cmdlet은 하나 이상의 파일을 **연결** 하 여 Data Lake store에 하나의 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="4bedf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4bedf-107">EXAMPLES</span></span>

### <span data-ttu-id="4bedf-108">예제 1: 두 항목 연결</span><span class="sxs-lookup"><span data-stu-id="4bedf-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="4bedf-109">이 명령은 File01.txt를 결합 하 고 File02.txt CombinedFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="4bedf-110">변수</span><span class="sxs-lookup"><span data-stu-id="4bedf-110">PARAMETERS</span></span>

### <span data-ttu-id="4bedf-111">-계정</span><span class="sxs-lookup"><span data-stu-id="4bedf-111">-Account</span></span>
<span data-ttu-id="4bedf-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4bedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bedf-113">-DefaultProfile</span></span>
<span data-ttu-id="4bedf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bedf-115">-대상</span><span class="sxs-lookup"><span data-stu-id="4bedf-115">-Destination</span></span>
<span data-ttu-id="4bedf-116">루트 디렉터리 (/)부터 시작 하 여 조인 된 항목에 대 한 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4bedf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4bedf-117">-Force</span></span>
<span data-ttu-id="4bedf-118">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="4bedf-119">-경로</span><span class="sxs-lookup"><span data-stu-id="4bedf-119">-Paths</span></span>
<span data-ttu-id="4bedf-120">루트 디렉터리 (/)로 시작 하 여 결합할 파일의 Data Lake Store 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bedf-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4bedf-121">-Confirm</span></span>
<span data-ttu-id="4bedf-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bedf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bedf-123">-WhatIf</span></span>
<span data-ttu-id="4bedf-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bedf-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bedf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bedf-126">CommonParameters</span></span>
<span data-ttu-id="4bedf-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bedf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bedf-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bedf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bedf-129">입력</span><span class="sxs-lookup"><span data-stu-id="4bedf-129">INPUTS</span></span>

### <span data-ttu-id="4bedf-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bedf-130">System.String</span></span>

### <span data-ttu-id="4bedf-131">DataLakeStore [] DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="4bedf-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="4bedf-132">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="4bedf-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4bedf-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4bedf-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4bedf-134">출력</span><span class="sxs-lookup"><span data-stu-id="4bedf-134">OUTPUTS</span></span>

### <span data-ttu-id="4bedf-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bedf-135">System.String</span></span>

## <span data-ttu-id="4bedf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4bedf-136">NOTES</span></span>

## <span data-ttu-id="4bedf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bedf-137">RELATED LINKS</span></span>

[<span data-ttu-id="4bedf-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="4bedf-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="4bedf-140">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="4bedf-141">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="4bedf-142">제거-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="4bedf-143">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4bedf-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


