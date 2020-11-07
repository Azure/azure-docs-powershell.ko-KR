---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701459"
---
# <span data-ttu-id="70d61-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="70d61-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="70d61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d61-102">SYNOPSIS</span></span>
<span data-ttu-id="70d61-103">일괄 처리 계정에서 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="70d61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70d61-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70d61-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70d61-105">DESCRIPTION</span></span>
<span data-ttu-id="70d61-106">**AzBatchApplication** Cmdlet은 Azure Batch 계정에서 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="70d61-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70d61-107">EXAMPLES</span></span>

### <span data-ttu-id="70d61-108">예제 1: 일괄 처리 계정에서 응용 프로그램 삭제</span><span class="sxs-lookup"><span data-stu-id="70d61-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="70d61-109">이 명령은 ContosoBatch 계정에서 Litware 응용 프로그램을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="70d61-110">응용 프로그램에 패키지가 포함 되어 있으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="70d61-111">변수</span><span class="sxs-lookup"><span data-stu-id="70d61-111">PARAMETERS</span></span>

### <span data-ttu-id="70d61-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70d61-112">-AccountName</span></span>
<span data-ttu-id="70d61-113">이 cmdlet이 응용 프로그램을 제거 하는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70d61-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="70d61-114">-ApplicationId</span></span>
<span data-ttu-id="70d61-115">응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70d61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d61-116">-DefaultProfile</span></span>
<span data-ttu-id="70d61-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70d61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d61-118">-ResourceGroupName</span></span>
<span data-ttu-id="70d61-119">일괄 처리 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70d61-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d61-120">CommonParameters</span></span>
<span data-ttu-id="70d61-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70d61-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d61-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d61-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d61-123">입력</span><span class="sxs-lookup"><span data-stu-id="70d61-123">INPUTS</span></span>

### <span data-ttu-id="70d61-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70d61-124">System.String</span></span>

## <span data-ttu-id="70d61-125">출력</span><span class="sxs-lookup"><span data-stu-id="70d61-125">OUTPUTS</span></span>

### <span data-ttu-id="70d61-126">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="70d61-126">System.Void</span></span>

## <span data-ttu-id="70d61-127">상속자</span><span class="sxs-lookup"><span data-stu-id="70d61-127">NOTES</span></span>

## <span data-ttu-id="70d61-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70d61-128">RELATED LINKS</span></span>

[<span data-ttu-id="70d61-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="70d61-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="70d61-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="70d61-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="70d61-131">새로운 AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="70d61-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="70d61-132">새로운 AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="70d61-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="70d61-133">제거-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="70d61-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="70d61-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="70d61-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


