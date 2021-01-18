---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494664"
---
# <span data-ttu-id="3ab08-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3ab08-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="3ab08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab08-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab08-103">저장소 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-103">Removes a storage table.</span></span>

## <span data-ttu-id="3ab08-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ab08-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab08-105">설명</span><span class="sxs-lookup"><span data-stu-id="3ab08-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab08-106">**Remove-AzStorageTable** cmdlet은 Azure의 저장소 계정에서 하나 이상의 저장소 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="3ab08-107">예제</span><span class="sxs-lookup"><span data-stu-id="3ab08-107">EXAMPLES</span></span>

### <span data-ttu-id="3ab08-108">예제 1: 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="3ab08-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="3ab08-109">이 명령은 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-109">This command removes a table.</span></span>

### <span data-ttu-id="3ab08-110">예제 2: 여러 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="3ab08-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="3ab08-111">이 예제에서는 *이름* 매개 변수가 있는 와일드카드 문자를 사용하여 패턴 테이블과 일치하는 모든 테이블을 선택한 다음 파이프라인에 결과를 전달하여 테이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="3ab08-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ab08-112">PARAMETERS</span></span>

### <span data-ttu-id="3ab08-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3ab08-113">-Context</span></span>
<span data-ttu-id="3ab08-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3ab08-115">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ab08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab08-116">-DefaultProfile</span></span>
<span data-ttu-id="3ab08-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab08-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3ab08-118">-Force</span></span>
<span data-ttu-id="3ab08-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ab08-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3ab08-120">-Name</span></span>
<span data-ttu-id="3ab08-121">제거할 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="3ab08-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ab08-122">-PassThru</span></span>
<span data-ttu-id="3ab08-123">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3ab08-124">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3ab08-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ab08-125">-Confirm</span></span>
<span data-ttu-id="3ab08-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab08-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab08-127">-WhatIf</span></span>
<span data-ttu-id="3ab08-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3ab08-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab08-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab08-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab08-130">CommonParameters</span></span>
<span data-ttu-id="3ab08-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab08-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab08-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3ab08-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab08-133">입력</span><span class="sxs-lookup"><span data-stu-id="3ab08-133">INPUTS</span></span>

### <span data-ttu-id="3ab08-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3ab08-134">System.String</span></span>

### <span data-ttu-id="3ab08-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ab08-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3ab08-136">출력</span><span class="sxs-lookup"><span data-stu-id="3ab08-136">OUTPUTS</span></span>

### <span data-ttu-id="3ab08-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ab08-137">System.Boolean</span></span>

## <span data-ttu-id="3ab08-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ab08-138">NOTES</span></span>

## <span data-ttu-id="3ab08-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ab08-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ab08-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="3ab08-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
