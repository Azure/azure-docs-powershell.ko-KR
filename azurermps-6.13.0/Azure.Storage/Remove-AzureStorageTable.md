---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: a4083920e935077658d218663e0a0255f6566ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702819"
---
# <span data-ttu-id="13396-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="13396-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="13396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13396-102">SYNOPSIS</span></span>
<span data-ttu-id="13396-103">저장소 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13396-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13396-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13396-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13396-105">DESCRIPTION</span></span>
<span data-ttu-id="13396-106">**AzureStorageTable** Cmdlet은 Azure의 저장소 계정에서 하나 이상의 저장소 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="13396-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13396-107">EXAMPLES</span></span>

### <span data-ttu-id="13396-108">예제 1: 표 제거</span><span class="sxs-lookup"><span data-stu-id="13396-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="13396-109">이 명령은 표를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-109">This command removes a table.</span></span>

### <span data-ttu-id="13396-110">예제 2: 여러 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="13396-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="13396-111">이 예제에서는 *Name* 매개 변수와 함께 와일드 카드 문자를 사용 하 여 패턴 테이블과 일치 하는 모든 테이블을 얻은 다음 파이프라인에 결과를 전달 하 여 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="13396-112">변수</span><span class="sxs-lookup"><span data-stu-id="13396-112">PARAMETERS</span></span>

### <span data-ttu-id="13396-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="13396-113">-Context</span></span>
<span data-ttu-id="13396-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="13396-115">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13396-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13396-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13396-116">-DefaultProfile</span></span>
<span data-ttu-id="13396-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13396-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13396-118">-Force</span><span class="sxs-lookup"><span data-stu-id="13396-118">-Force</span></span>
<span data-ttu-id="13396-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13396-120">-이름</span><span class="sxs-lookup"><span data-stu-id="13396-120">-Name</span></span>
<span data-ttu-id="13396-121">제거할 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13396-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13396-122">-PassThru</span></span>
<span data-ttu-id="13396-123">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13396-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="13396-124">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13396-124">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13396-125">-확인</span><span class="sxs-lookup"><span data-stu-id="13396-125">-Confirm</span></span>
<span data-ttu-id="13396-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13396-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13396-127">-WhatIf</span></span>
<span data-ttu-id="13396-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13396-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13396-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13396-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13396-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13396-130">CommonParameters</span></span>
<span data-ttu-id="13396-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13396-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13396-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13396-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13396-133">입력</span><span class="sxs-lookup"><span data-stu-id="13396-133">INPUTS</span></span>

### <span data-ttu-id="13396-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13396-134">System.String</span></span>

### <span data-ttu-id="13396-135">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="13396-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="13396-136">출력</span><span class="sxs-lookup"><span data-stu-id="13396-136">OUTPUTS</span></span>

### <span data-ttu-id="13396-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="13396-137">System.Boolean</span></span>

## <span data-ttu-id="13396-138">상속자</span><span class="sxs-lookup"><span data-stu-id="13396-138">NOTES</span></span>

## <span data-ttu-id="13396-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13396-139">RELATED LINKS</span></span>

[<span data-ttu-id="13396-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="13396-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
