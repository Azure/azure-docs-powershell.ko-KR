---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344301"
---
# <span data-ttu-id="b8535-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b8535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8535-102">SYNOPSIS</span></span>
<span data-ttu-id="b8535-103">Data Lake Store에서 파일 또는 폴더를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b8535-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8535-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8535-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8535-105">DESCRIPTION</span></span>
<span data-ttu-id="b8535-106">**Remove-AzDataLakeStoreItem** cmdlet은 Data Lake Store의 파일 또는 폴더를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b8535-107">예제</span><span class="sxs-lookup"><span data-stu-id="b8535-107">EXAMPLES</span></span>

### <span data-ttu-id="b8535-108">예제 1: 여러 항목 제거</span><span class="sxs-lookup"><span data-stu-id="b8535-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="b8535-109">이 명령은 Data Lake File01.txt File.csv 파일을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="b8535-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8535-110">PARAMETERS</span></span>

### <span data-ttu-id="b8535-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b8535-111">-Account</span></span>
<span data-ttu-id="b8535-112">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b8535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8535-113">-DefaultProfile</span></span>
<span data-ttu-id="b8535-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8535-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b8535-115">-Force</span></span>
<span data-ttu-id="b8535-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8535-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8535-117">-PassThru</span></span>
<span data-ttu-id="b8535-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b8535-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8535-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="b8535-120">-Paths</span></span>
<span data-ttu-id="b8535-121">루트 디렉터리(/)로 시작하여 제거할 파일의 Data Lake Store 경로 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8535-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b8535-122">-Recurse</span></span>
<span data-ttu-id="b8535-123">이 작업은 하위 폴더를 포함하여 대상 폴더의 모든 항목을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8535-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8535-124">-Confirm</span></span>
<span data-ttu-id="b8535-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8535-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8535-126">-WhatIf</span></span>
<span data-ttu-id="b8535-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b8535-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8535-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8535-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8535-129">CommonParameters</span></span>
<span data-ttu-id="b8535-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8535-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8535-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8535-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8535-132">입력</span><span class="sxs-lookup"><span data-stu-id="b8535-132">INPUTS</span></span>

### <span data-ttu-id="b8535-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b8535-133">System.String</span></span>

### <span data-ttu-id="b8535-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="b8535-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="b8535-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8535-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8535-136">출력</span><span class="sxs-lookup"><span data-stu-id="b8535-136">OUTPUTS</span></span>

### <span data-ttu-id="b8535-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8535-137">System.Boolean</span></span>

## <span data-ttu-id="b8535-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8535-138">NOTES</span></span>

## <span data-ttu-id="b8535-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8535-139">RELATED LINKS</span></span>

[<span data-ttu-id="b8535-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="b8535-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b8535-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b8535-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="b8535-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b8535-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b8535-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


