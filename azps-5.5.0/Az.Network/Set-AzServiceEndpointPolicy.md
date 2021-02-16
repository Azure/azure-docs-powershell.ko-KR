---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184148"
---
# <span data-ttu-id="cf414-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="cf414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf414-102">SYNOPSIS</span></span>
<span data-ttu-id="cf414-103">서비스 엔드포인트 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="cf414-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf414-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf414-105">설명</span><span class="sxs-lookup"><span data-stu-id="cf414-105">DESCRIPTION</span></span>
<span data-ttu-id="cf414-106">**Set-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="cf414-107">예제</span><span class="sxs-lookup"><span data-stu-id="cf414-107">EXAMPLES</span></span>

### <span data-ttu-id="cf414-108">예제 1: 서비스 엔드포인트 정책 설정</span><span class="sxs-lookup"><span data-stu-id="cf414-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="cf414-109">이 명령은 리소스 그룹 "resourcegroup1"에 속한 개체에 $serviceEndpointPolicy Policy1이라는 서비스 엔드포인트 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="cf414-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf414-110">PARAMETERS</span></span>

### <span data-ttu-id="cf414-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf414-111">-DefaultProfile</span></span>
<span data-ttu-id="cf414-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf414-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="cf414-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf414-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf414-115">-Confirm</span></span>
<span data-ttu-id="cf414-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf414-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf414-117">-WhatIf</span></span>
<span data-ttu-id="cf414-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cf414-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf414-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf414-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf414-120">CommonParameters</span></span>
<span data-ttu-id="cf414-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf414-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf414-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cf414-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf414-123">입력</span><span class="sxs-lookup"><span data-stu-id="cf414-123">INPUTS</span></span>

### <span data-ttu-id="cf414-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cf414-125">출력</span><span class="sxs-lookup"><span data-stu-id="cf414-125">OUTPUTS</span></span>

### <span data-ttu-id="cf414-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cf414-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf414-127">NOTES</span></span>

## <span data-ttu-id="cf414-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf414-128">RELATED LINKS</span></span>

[<span data-ttu-id="cf414-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cf414-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cf414-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf414-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
