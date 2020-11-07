---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 3b66cdc6574397de7d43dfef0677a5ddac772a31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701340"
---
# <span data-ttu-id="2f3b0-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2f3b0-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="2f3b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3b0-103">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-103">Get a run command document.</span></span>

## <span data-ttu-id="2f3b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f3b0-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f3b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3b0-106">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-106">Get a run command document.</span></span>

## <span data-ttu-id="2f3b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2f3b0-107">EXAMPLES</span></span>

### <span data-ttu-id="2f3b0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f3b0-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="2f3b0-109">' Westus '의 ' RunPowerShellScript '에 대 한 특정 실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="2f3b0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2f3b0-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="2f3b0-111">' Westus '에 사용 가능한 모든 실행 명령을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="2f3b0-112">변수</span><span class="sxs-lookup"><span data-stu-id="2f3b0-112">PARAMETERS</span></span>

### <span data-ttu-id="2f3b0-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2f3b0-113">-CommandId</span></span>
<span data-ttu-id="2f3b0-114">명령 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-114">The command ID.</span></span>

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

### <span data-ttu-id="2f3b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3b0-115">-DefaultProfile</span></span>
<span data-ttu-id="2f3b0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f3b0-117">-위치</span><span class="sxs-lookup"><span data-stu-id="2f3b0-117">-Location</span></span>
<span data-ttu-id="2f3b0-118">실행 명령이 쿼리 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="2f3b0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3b0-119">CommonParameters</span></span>
<span data-ttu-id="2f3b0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3b0-121">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2f3b0-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3b0-122">입력</span><span class="sxs-lookup"><span data-stu-id="2f3b0-122">INPUTS</span></span>

### <span data-ttu-id="2f3b0-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2f3b0-123">System.String</span></span>

## <span data-ttu-id="2f3b0-124">출력</span><span class="sxs-lookup"><span data-stu-id="2f3b0-124">OUTPUTS</span></span>

### <span data-ttu-id="2f3b0-125">Microsoft. a. m a. 모델. a PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2f3b0-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="2f3b0-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2f3b0-126">NOTES</span></span>

## <span data-ttu-id="2f3b0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f3b0-127">RELATED LINKS</span></span>