---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 86d8e3bfebe8e87abacc78859dd6e776ff2ccf0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981003"
---
# <span data-ttu-id="653cc-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="653cc-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="653cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="653cc-102">SYNOPSIS</span></span>
<span data-ttu-id="653cc-103">실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-103">Get a run command document.</span></span>

## <span data-ttu-id="653cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="653cc-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="653cc-105">설명</span><span class="sxs-lookup"><span data-stu-id="653cc-105">DESCRIPTION</span></span>
<span data-ttu-id="653cc-106">실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-106">Get a run command document.</span></span>

## <span data-ttu-id="653cc-107">예제</span><span class="sxs-lookup"><span data-stu-id="653cc-107">EXAMPLES</span></span>

### <span data-ttu-id="653cc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="653cc-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="653cc-109">'westus'에서 'RunPowerShellScript'에 대한 특정 실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="653cc-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="653cc-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="653cc-111">사용 가능한 모든 실행 명령을 'westus'에 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="653cc-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="653cc-112">PARAMETERS</span></span>

### <span data-ttu-id="653cc-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="653cc-113">-CommandId</span></span>
<span data-ttu-id="653cc-114">명령 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-114">The command ID.</span></span>

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

### <span data-ttu-id="653cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653cc-115">-DefaultProfile</span></span>
<span data-ttu-id="653cc-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="653cc-117">-Location</span><span class="sxs-lookup"><span data-stu-id="653cc-117">-Location</span></span>
<span data-ttu-id="653cc-118">실행 명령이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="653cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653cc-119">CommonParameters</span></span>
<span data-ttu-id="653cc-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="653cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653cc-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="653cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653cc-122">입력</span><span class="sxs-lookup"><span data-stu-id="653cc-122">INPUTS</span></span>

### <span data-ttu-id="653cc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="653cc-123">System.String</span></span>

## <span data-ttu-id="653cc-124">출력</span><span class="sxs-lookup"><span data-stu-id="653cc-124">OUTPUTS</span></span>

### <span data-ttu-id="653cc-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="653cc-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="653cc-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="653cc-126">NOTES</span></span>

## <span data-ttu-id="653cc-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="653cc-127">RELATED LINKS</span></span>
