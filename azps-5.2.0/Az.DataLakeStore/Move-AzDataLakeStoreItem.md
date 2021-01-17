---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347505"
---
# <span data-ttu-id="932c3-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="932c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="932c3-102">SYNOPSIS</span></span>
<span data-ttu-id="932c3-103">Data Lake Store에서 파일 또는 폴더를 이동하거나 이름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="932c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="932c3-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="932c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="932c3-105">DESCRIPTION</span></span>
<span data-ttu-id="932c3-106">**Move-AzDataLakeStoreItem** cmdlet은 Data Lake Store에서 파일 또는 폴더를 이동하거나 이름을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="932c3-107">예제</span><span class="sxs-lookup"><span data-stu-id="932c3-107">EXAMPLES</span></span>

### <span data-ttu-id="932c3-108">예제 1: 항목 이동 및 이름 바</span><span class="sxs-lookup"><span data-stu-id="932c3-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="932c3-109">이 명령은 항목 이름을 File.txt RenamedFile.txt 다른 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="932c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="932c3-110">PARAMETERS</span></span>

### <span data-ttu-id="932c3-111">-Account</span><span class="sxs-lookup"><span data-stu-id="932c3-111">-Account</span></span>
<span data-ttu-id="932c3-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="932c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932c3-113">-DefaultProfile</span></span>
<span data-ttu-id="932c3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="932c3-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="932c3-115">-Destination</span></span>
<span data-ttu-id="932c3-116">루트 디렉터리(/)로 시작하여 항목을 이동할 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="932c3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="932c3-117">-Force</span></span>
<span data-ttu-id="932c3-118">이 작업이 대상 파일이 이미 있는 경우 대상 파일을 덮어써도 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="932c3-119">-Path</span><span class="sxs-lookup"><span data-stu-id="932c3-119">-Path</span></span>
<span data-ttu-id="932c3-120">루트 디렉터리(/)로 시작하여 이동하거나 이름을 변경하는 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="932c3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="932c3-121">-Confirm</span></span>
<span data-ttu-id="932c3-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="932c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="932c3-123">-WhatIf</span></span>
<span data-ttu-id="932c3-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="932c3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="932c3-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="932c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932c3-126">CommonParameters</span></span>
<span data-ttu-id="932c3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="932c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932c3-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="932c3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932c3-129">입력</span><span class="sxs-lookup"><span data-stu-id="932c3-129">INPUTS</span></span>

### <span data-ttu-id="932c3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="932c3-130">System.String</span></span>

### <span data-ttu-id="932c3-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="932c3-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="932c3-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="932c3-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="932c3-133">출력</span><span class="sxs-lookup"><span data-stu-id="932c3-133">OUTPUTS</span></span>

### <span data-ttu-id="932c3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="932c3-134">System.String</span></span>

## <span data-ttu-id="932c3-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="932c3-135">NOTES</span></span>

## <span data-ttu-id="932c3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="932c3-136">RELATED LINKS</span></span>

[<span data-ttu-id="932c3-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="932c3-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="932c3-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="932c3-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="932c3-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="932c3-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="932c3-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


