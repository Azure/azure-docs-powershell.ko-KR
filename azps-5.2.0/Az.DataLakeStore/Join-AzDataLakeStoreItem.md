---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361166"
---
# <span data-ttu-id="7111f-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="7111f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7111f-102">SYNOPSIS</span></span>
<span data-ttu-id="7111f-103">하나 이상의 파일을 조인하여 Data Lake Store에서 파일을 하나 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="7111f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7111f-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7111f-105">설명</span><span class="sxs-lookup"><span data-stu-id="7111f-105">DESCRIPTION</span></span>
<span data-ttu-id="7111f-106">**Join-AzDataLakeStoreItem** cmdlet은 하나 이상의 파일을 조인하여 Data Lake Store에 파일을 하나씩 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="7111f-107">예제</span><span class="sxs-lookup"><span data-stu-id="7111f-107">EXAMPLES</span></span>

### <span data-ttu-id="7111f-108">예제 1: 두 항목 조인</span><span class="sxs-lookup"><span data-stu-id="7111f-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="7111f-109">이 명령은 File01.txt File02.txt 파일을 만들 수 CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="7111f-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="7111f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7111f-110">PARAMETERS</span></span>

### <span data-ttu-id="7111f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7111f-111">-Account</span></span>
<span data-ttu-id="7111f-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7111f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7111f-113">-DefaultProfile</span></span>
<span data-ttu-id="7111f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7111f-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="7111f-115">-Destination</span></span>
<span data-ttu-id="7111f-116">루트 디렉터리(/)로 시작하는 조인된 항목에 대한 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7111f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7111f-117">-Force</span></span>
<span data-ttu-id="7111f-118">이 작업이 대상 파일이 이미 있는 경우 대상 파일을 덮어써도 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="7111f-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="7111f-119">-Paths</span></span>
<span data-ttu-id="7111f-120">루트 디렉터리(/)로 시작하여 결합할 파일의 Data Lake Store 경로 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7111f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7111f-121">-Confirm</span></span>
<span data-ttu-id="7111f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7111f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7111f-123">-WhatIf</span></span>
<span data-ttu-id="7111f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7111f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7111f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7111f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7111f-126">CommonParameters</span></span>
<span data-ttu-id="7111f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7111f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7111f-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7111f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7111f-129">입력</span><span class="sxs-lookup"><span data-stu-id="7111f-129">INPUTS</span></span>

### <span data-ttu-id="7111f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7111f-130">System.String</span></span>

### <span data-ttu-id="7111f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="7111f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="7111f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7111f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7111f-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7111f-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7111f-134">출력</span><span class="sxs-lookup"><span data-stu-id="7111f-134">OUTPUTS</span></span>

### <span data-ttu-id="7111f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7111f-135">System.String</span></span>

## <span data-ttu-id="7111f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7111f-136">NOTES</span></span>

## <span data-ttu-id="7111f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7111f-137">RELATED LINKS</span></span>

[<span data-ttu-id="7111f-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="7111f-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="7111f-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="7111f-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="7111f-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="7111f-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7111f-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


