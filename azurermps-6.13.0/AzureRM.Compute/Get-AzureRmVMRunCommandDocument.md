---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: 070fe50f74db08caab375a97d4d8ff6be3e970ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529621"
---
# <span data-ttu-id="b46f8-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b46f8-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="b46f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b46f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b46f8-103">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b46f8-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b46f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b46f8-105">DESCRIPTION</span></span>
<span data-ttu-id="b46f8-106">실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-106">Get run command document.</span></span>

## <span data-ttu-id="b46f8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b46f8-107">EXAMPLES</span></span>

### <span data-ttu-id="b46f8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b46f8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="b46f8-109">' Westus '의 ' RunPowerShellScript '에 대 한 특정 실행 명령 문서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>
<span data-ttu-id="b46f8-110">Get-AzureRmVMRunCommandDocument 위치 $loc</span><span class="sxs-lookup"><span data-stu-id="b46f8-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="b46f8-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="b46f8-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="b46f8-112">' Westus '에 사용 가능한 모든 실행 명령을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="b46f8-113">변수</span><span class="sxs-lookup"><span data-stu-id="b46f8-113">PARAMETERS</span></span>

### <span data-ttu-id="b46f8-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="b46f8-114">-CommandId</span></span>
<span data-ttu-id="b46f8-115">명령 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b46f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46f8-116">-DefaultProfile</span></span>
<span data-ttu-id="b46f8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b46f8-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b46f8-118">-Location</span></span>
<span data-ttu-id="b46f8-119">실행 명령이 쿼리 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="b46f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46f8-120">CommonParameters</span></span>
<span data-ttu-id="b46f8-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b46f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46f8-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b46f8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46f8-123">입력</span><span class="sxs-lookup"><span data-stu-id="b46f8-123">INPUTS</span></span>

### <span data-ttu-id="b46f8-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b46f8-124">System.String</span></span>

## <span data-ttu-id="b46f8-125">출력</span><span class="sxs-lookup"><span data-stu-id="b46f8-125">OUTPUTS</span></span>

### <span data-ttu-id="b46f8-126">Microsoft. a. m a. 모델. a PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b46f8-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="b46f8-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b46f8-127">NOTES</span></span>

## <span data-ttu-id="b46f8-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b46f8-128">RELATED LINKS</span></span>
