---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703069"
---
# <span data-ttu-id="b3572-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b3572-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="b3572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3572-102">SYNOPSIS</span></span>
<span data-ttu-id="b3572-103">저장소 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3572-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3572-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3572-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3572-105">DESCRIPTION</span></span>
<span data-ttu-id="b3572-106">**AzureStorageTable** Cmdlet은 Azure의 저장소 계정에서 하나 이상의 저장소 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="b3572-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3572-107">EXAMPLES</span></span>

### <span data-ttu-id="b3572-108">예제 1: 표 제거</span><span class="sxs-lookup"><span data-stu-id="b3572-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="b3572-109">이 명령은 표를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-109">This command removes a table.</span></span>

### <span data-ttu-id="b3572-110">예제 2: 여러 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="b3572-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="b3572-111">이 예제에서는 *Name* 매개 변수와 함께 와일드 카드 문자를 사용 하 여 패턴 테이블과 일치 하는 모든 테이블을 얻은 다음 파이프라인에 결과를 전달 하 여 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="b3572-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3572-112">PARAMETERS</span></span>

### <span data-ttu-id="b3572-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b3572-113">-Context</span></span>
<span data-ttu-id="b3572-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b3572-115">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b3572-116">-Force</span></span>
<span data-ttu-id="b3572-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b3572-118">-Name</span></span>
<span data-ttu-id="b3572-119">제거할 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3572-120">-PassThru</span></span>
<span data-ttu-id="b3572-121">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b3572-122">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b3572-123">-Confirm</span></span>
<span data-ttu-id="b3572-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3572-125">-WhatIf</span></span>
<span data-ttu-id="b3572-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3572-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3572-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3572-128">CommonParameters</span></span>
<span data-ttu-id="b3572-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3572-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3572-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3572-131">입력</span><span class="sxs-lookup"><span data-stu-id="b3572-131">INPUTS</span></span>

### <span data-ttu-id="b3572-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3572-132">IStorageContext</span></span>

<span data-ttu-id="b3572-133">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b3572-134">이름</span><span class="sxs-lookup"><span data-stu-id="b3572-134">String</span></span>

<span data-ttu-id="b3572-135">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3572-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b3572-136">출력</span><span class="sxs-lookup"><span data-stu-id="b3572-136">OUTPUTS</span></span>

### <span data-ttu-id="b3572-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b3572-137">System.Boolean</span></span>

## <span data-ttu-id="b3572-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b3572-138">NOTES</span></span>

## <span data-ttu-id="b3572-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3572-139">RELATED LINKS</span></span>

[<span data-ttu-id="b3572-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b3572-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
