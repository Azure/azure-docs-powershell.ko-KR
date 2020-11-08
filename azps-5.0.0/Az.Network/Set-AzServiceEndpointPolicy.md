---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217585"
---
# <span data-ttu-id="4efe8-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="4efe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4efe8-102">SYNOPSIS</span></span>
<span data-ttu-id="4efe8-103">서비스 끝점 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="4efe8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4efe8-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efe8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4efe8-105">DESCRIPTION</span></span>
<span data-ttu-id="4efe8-106">**AzServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4efe8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4efe8-107">EXAMPLES</span></span>

### <span data-ttu-id="4efe8-108">예제 1: 서비스 끝점 정책 설정</span><span class="sxs-lookup"><span data-stu-id="4efe8-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4efe8-109">이 명령은 Policy1 "resourcegroup1"에 속하는 개체 $serviceEndpointPolicy 정의 된 서비스 끝점 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4efe8-110">변수</span><span class="sxs-lookup"><span data-stu-id="4efe8-110">PARAMETERS</span></span>

### <span data-ttu-id="4efe8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efe8-111">-DefaultProfile</span></span>
<span data-ttu-id="4efe8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efe8-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4efe8-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4efe8-115">-확인</span><span class="sxs-lookup"><span data-stu-id="4efe8-115">-Confirm</span></span>
<span data-ttu-id="4efe8-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4efe8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efe8-117">-WhatIf</span></span>
<span data-ttu-id="4efe8-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4efe8-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4efe8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efe8-120">CommonParameters</span></span>
<span data-ttu-id="4efe8-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4efe8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efe8-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efe8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efe8-123">입력</span><span class="sxs-lookup"><span data-stu-id="4efe8-123">INPUTS</span></span>

### <span data-ttu-id="4efe8-124">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4efe8-125">출력</span><span class="sxs-lookup"><span data-stu-id="4efe8-125">OUTPUTS</span></span>

### <span data-ttu-id="4efe8-126">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4efe8-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4efe8-127">NOTES</span></span>

## <span data-ttu-id="4efe8-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4efe8-128">RELATED LINKS</span></span>

[<span data-ttu-id="4efe8-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4efe8-130">새로운 AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4efe8-131">제거-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4efe8-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
