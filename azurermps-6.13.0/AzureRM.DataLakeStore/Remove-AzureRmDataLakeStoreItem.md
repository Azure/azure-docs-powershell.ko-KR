---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 03e43530a044bad5f3ea7509fa649da9f26a93f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524455"
---
# <span data-ttu-id="7a6bf-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="7a6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6bf-103">Data Lake Store에서 파일 또는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a6bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a6bf-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a6bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6bf-106">**AzureRmDataLakeStoreItem** Cmdlet은 Data Lake store에서 파일 또는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7a6bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6bf-108">예제 1: 여러 항목 제거</span><span class="sxs-lookup"><span data-stu-id="7a6bf-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="7a6bf-109">이 명령은 File01.txt 파일을 제거 하 고 Data Lake Store에서 File.csv 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="7a6bf-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a6bf-110">PARAMETERS</span></span>

### <span data-ttu-id="7a6bf-111">-계정</span><span class="sxs-lookup"><span data-stu-id="7a6bf-111">-Account</span></span>
<span data-ttu-id="7a6bf-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7a6bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6bf-113">-DefaultProfile</span></span>
<span data-ttu-id="7a6bf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a6bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a6bf-115">-Force</span></span>
<span data-ttu-id="7a6bf-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a6bf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a6bf-117">-PassThru</span></span>
<span data-ttu-id="7a6bf-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a6bf-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a6bf-120">-경로</span><span class="sxs-lookup"><span data-stu-id="7a6bf-120">-Paths</span></span>
<span data-ttu-id="7a6bf-121">루트 디렉터리 (/)로 시작 하는 제거할 파일의 Data Lake Store 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7a6bf-122">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="7a6bf-122">-Recurse</span></span>
<span data-ttu-id="7a6bf-123">이 작업이 하위 폴더를 포함 하 여 대상 폴더의 모든 항목을 삭제 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="7a6bf-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7a6bf-124">-Confirm</span></span>
<span data-ttu-id="7a6bf-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6bf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6bf-126">-WhatIf</span></span>
<span data-ttu-id="7a6bf-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6bf-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6bf-129">CommonParameters</span></span>
<span data-ttu-id="7a6bf-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a6bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6bf-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a6bf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6bf-132">입력</span><span class="sxs-lookup"><span data-stu-id="7a6bf-132">INPUTS</span></span>

### <span data-ttu-id="7a6bf-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a6bf-133">System.String</span></span>

### <span data-ttu-id="7a6bf-134">DataLakeStore [] DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="7a6bf-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="7a6bf-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a6bf-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a6bf-136">출력</span><span class="sxs-lookup"><span data-stu-id="7a6bf-136">OUTPUTS</span></span>

### <span data-ttu-id="7a6bf-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7a6bf-137">System.Boolean</span></span>

## <span data-ttu-id="7a6bf-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7a6bf-138">NOTES</span></span>

## <span data-ttu-id="7a6bf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a6bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a6bf-140">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-140">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7a6bf-141">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-141">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7a6bf-142">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-142">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7a6bf-143">참가-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-143">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7a6bf-144">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-144">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7a6bf-145">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7a6bf-145">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


