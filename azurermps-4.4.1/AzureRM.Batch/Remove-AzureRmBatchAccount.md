---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3de75d2c8e7ed69a8f5be02833dd002ee5fbf016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532339"
---
# <span data-ttu-id="2d459-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2d459-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="2d459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d459-102">SYNOPSIS</span></span>
<span data-ttu-id="2d459-103">일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d459-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d459-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d459-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d459-105">DESCRIPTION</span></span>
<span data-ttu-id="2d459-106">**AzureRmBatchAccount** Cmdlet은 Azure Batch 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="2d459-107">이 cmdlet은 *Force* 매개 변수를 지정 하지 않는 한 계정을 제거 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="2d459-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2d459-108">EXAMPLES</span></span>

### <span data-ttu-id="2d459-109">예제 1: 일괄 처리 계정 제거</span><span class="sxs-lookup"><span data-stu-id="2d459-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="2d459-110">이 명령은 pfuller 이름의 일괄 처리 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="2d459-111">이 명령은 계정을 삭제 하기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="2d459-112">변수</span><span class="sxs-lookup"><span data-stu-id="2d459-112">PARAMETERS</span></span>

### <span data-ttu-id="2d459-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d459-113">-AccountName</span></span>
<span data-ttu-id="2d459-114">이 cmdlet이 제거 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d459-115">-Force</span></span>
<span data-ttu-id="2d459-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d459-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d459-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d459-118">이 cmdlet이 제거 하는 계정의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-118">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d459-119">-확인</span><span class="sxs-lookup"><span data-stu-id="2d459-119">-Confirm</span></span>
<span data-ttu-id="2d459-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d459-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d459-121">-WhatIf</span></span>
<span data-ttu-id="2d459-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d459-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d459-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d459-124">-DefaultProfile</span></span>
<span data-ttu-id="2d459-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d459-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d459-126">CommonParameters</span></span>
<span data-ttu-id="2d459-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d459-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d459-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d459-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d459-129">입력</span><span class="sxs-lookup"><span data-stu-id="2d459-129">INPUTS</span></span>

## <span data-ttu-id="2d459-130">출력</span><span class="sxs-lookup"><span data-stu-id="2d459-130">OUTPUTS</span></span>

## <span data-ttu-id="2d459-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2d459-131">NOTES</span></span>

## <span data-ttu-id="2d459-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d459-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d459-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2d459-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="2d459-134">새로운 AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2d459-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="2d459-135">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2d459-135">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="2d459-136">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d459-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


