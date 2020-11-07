---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 1ad6fbd77bc827b1cccd3074198182489186d06b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701058"
---
# <span data-ttu-id="0ea1a-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="0ea1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea1a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea1a-103">Data Lake Store에서 파일 또는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0ea1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ea1a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea1a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ea1a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ea1a-106">**AzDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일 또는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0ea1a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ea1a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ea1a-108">예제 1: 여러 항목 제거</span><span class="sxs-lookup"><span data-stu-id="0ea1a-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="0ea1a-109">이 명령은 File01.txt 파일을 제거 하 고 Data Lake Store에서 File.csv 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="0ea1a-110">변수</span><span class="sxs-lookup"><span data-stu-id="0ea1a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ea1a-111">-계정</span><span class="sxs-lookup"><span data-stu-id="0ea1a-111">-Account</span></span>
<span data-ttu-id="0ea1a-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0ea1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea1a-113">-DefaultProfile</span></span>
<span data-ttu-id="0ea1a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea1a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0ea1a-115">-Force</span></span>
<span data-ttu-id="0ea1a-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ea1a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ea1a-117">-PassThru</span></span>
<span data-ttu-id="0ea1a-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ea1a-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ea1a-120">-경로</span><span class="sxs-lookup"><span data-stu-id="0ea1a-120">-Paths</span></span>
<span data-ttu-id="0ea1a-121">루트 디렉터리 (/)로 시작 하는 제거할 파일의 Data Lake Store 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0ea1a-122">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="0ea1a-122">-Recurse</span></span>
<span data-ttu-id="0ea1a-123">이 작업이 하위 폴더를 포함 하 여 대상 폴더의 모든 항목을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="0ea1a-124">-확인</span><span class="sxs-lookup"><span data-stu-id="0ea1a-124">-Confirm</span></span>
<span data-ttu-id="0ea1a-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea1a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea1a-126">-WhatIf</span></span>
<span data-ttu-id="0ea1a-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea1a-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea1a-129">CommonParameters</span></span>
<span data-ttu-id="0ea1a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ea1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea1a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea1a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea1a-132">입력</span><span class="sxs-lookup"><span data-stu-id="0ea1a-132">INPUTS</span></span>

### <span data-ttu-id="0ea1a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ea1a-133">System.String</span></span>

### <span data-ttu-id="0ea1a-134">DataLakeStore [] DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="0ea1a-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="0ea1a-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ea1a-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ea1a-136">출력</span><span class="sxs-lookup"><span data-stu-id="0ea1a-136">OUTPUTS</span></span>

### <span data-ttu-id="0ea1a-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0ea1a-137">System.Boolean</span></span>

## <span data-ttu-id="0ea1a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0ea1a-138">NOTES</span></span>

## <span data-ttu-id="0ea1a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ea1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ea1a-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea1a-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea1a-142">가져오기-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea1a-143">참가-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea1a-144">새로운 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="0ea1a-145">테스트-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0ea1a-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

