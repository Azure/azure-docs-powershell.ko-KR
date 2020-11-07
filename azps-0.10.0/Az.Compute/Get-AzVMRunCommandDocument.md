---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877048"
---
# <span data-ttu-id="f1e5a-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f1e5a-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="f1e5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e5a-103">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-103">Get run command document.</span></span>

## <span data-ttu-id="f1e5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1e5a-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1e5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e5a-106">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-106">Get run command document.</span></span>

## <span data-ttu-id="f1e5a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f1e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e5a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1e5a-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="f1e5a-109">' Westus '의 ' RunPowerShellScript '에 대 한 특정 실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="f1e5a-110">Get-AzVMRunCommandDocument 위치 $loc</span><span class="sxs-lookup"><span data-stu-id="f1e5a-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="f1e5a-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1e5a-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="f1e5a-112">' Westus '에 사용 가능한 모든 실행 명령을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="f1e5a-113">변수</span><span class="sxs-lookup"><span data-stu-id="f1e5a-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e5a-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="f1e5a-114">-CommandId</span></span>
<span data-ttu-id="f1e5a-115">명령 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e5a-116">-DefaultProfile</span></span>
<span data-ttu-id="f1e5a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e5a-118">-위치</span><span class="sxs-lookup"><span data-stu-id="f1e5a-118">-Location</span></span>
<span data-ttu-id="f1e5a-119">실행 명령이 쿼리 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e5a-120">CommonParameters</span></span>
<span data-ttu-id="f1e5a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1e5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e5a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e5a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e5a-123">입력</span><span class="sxs-lookup"><span data-stu-id="f1e5a-123">INPUTS</span></span>

### <span data-ttu-id="f1e5a-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1e5a-124">System.String</span></span>

## <span data-ttu-id="f1e5a-125">출력</span><span class="sxs-lookup"><span data-stu-id="f1e5a-125">OUTPUTS</span></span>

### <span data-ttu-id="f1e5a-126">Microsoft. a. m a. 모델. a PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="f1e5a-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="f1e5a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f1e5a-127">NOTES</span></span>

## <span data-ttu-id="f1e5a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1e5a-128">RELATED LINKS</span></span>

