---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3e460cddb83eacc1a012aebd009cd087ba1b68d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536116"
---
# <span data-ttu-id="75442-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75442-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="75442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75442-102">SYNOPSIS</span></span>
<span data-ttu-id="75442-103">일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75442-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75442-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75442-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75442-105">DESCRIPTION</span></span>
<span data-ttu-id="75442-106">**AzureRmBatchAccount** Cmdlet은 Azure Batch 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="75442-107">이 cmdlet은 *Force* 매개 변수를 지정 하지 않는 한 계정을 제거 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="75442-108">예제의</span><span class="sxs-lookup"><span data-stu-id="75442-108">EXAMPLES</span></span>

### <span data-ttu-id="75442-109">예제 1: 일괄 처리 계정 제거</span><span class="sxs-lookup"><span data-stu-id="75442-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="75442-110">이 명령은 pfuller 이름의 일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="75442-111">이 명령은 계정을 삭제 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="75442-112">변수</span><span class="sxs-lookup"><span data-stu-id="75442-112">PARAMETERS</span></span>

### <span data-ttu-id="75442-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75442-113">-AccountName</span></span>
<span data-ttu-id="75442-114">이 cmdlet이 제거 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75442-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75442-115">-DefaultProfile</span></span>
<span data-ttu-id="75442-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75442-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75442-117">-Force</span><span class="sxs-lookup"><span data-stu-id="75442-117">-Force</span></span>
<span data-ttu-id="75442-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75442-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75442-119">-ResourceGroupName</span></span>
<span data-ttu-id="75442-120">이 cmdlet이 제거 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75442-121">-확인</span><span class="sxs-lookup"><span data-stu-id="75442-121">-Confirm</span></span>
<span data-ttu-id="75442-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75442-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75442-123">-WhatIf</span></span>
<span data-ttu-id="75442-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75442-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75442-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75442-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75442-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75442-126">CommonParameters</span></span>
<span data-ttu-id="75442-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75442-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75442-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75442-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75442-129">입력</span><span class="sxs-lookup"><span data-stu-id="75442-129">INPUTS</span></span>

### <span data-ttu-id="75442-130">않아야</span><span class="sxs-lookup"><span data-stu-id="75442-130">None</span></span>
<span data-ttu-id="75442-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75442-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75442-132">출력</span><span class="sxs-lookup"><span data-stu-id="75442-132">OUTPUTS</span></span>

## <span data-ttu-id="75442-133">상속자</span><span class="sxs-lookup"><span data-stu-id="75442-133">NOTES</span></span>

## <span data-ttu-id="75442-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75442-134">RELATED LINKS</span></span>

[<span data-ttu-id="75442-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75442-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="75442-136">새로운 AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75442-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="75442-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="75442-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="75442-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75442-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


