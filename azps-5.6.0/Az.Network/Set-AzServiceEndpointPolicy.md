---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: e8cf8b2abebd20b514d0bae2ad220d3e702f04f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008704"
---
# <span data-ttu-id="ed315-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ed315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed315-102">SYNOPSIS</span></span>
<span data-ttu-id="ed315-103">서비스 엔드포인트 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="ed315-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed315-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed315-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed315-105">DESCRIPTION</span></span>
<span data-ttu-id="ed315-106">**Set-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="ed315-107">예제</span><span class="sxs-lookup"><span data-stu-id="ed315-107">EXAMPLES</span></span>

### <span data-ttu-id="ed315-108">예제 1: 서비스 엔드포인트 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ed315-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ed315-109">이 명령은 개체가 정의한 Policy1이라는 서비스 엔드포인트 정책을 $serviceEndpointPolicy 리소스 그룹 "resourcegroup1"에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="ed315-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed315-110">PARAMETERS</span></span>

### <span data-ttu-id="ed315-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed315-111">-DefaultProfile</span></span>
<span data-ttu-id="ed315-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed315-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ed315-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="ed315-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ed315-115">-Confirm</span></span>
<span data-ttu-id="ed315-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed315-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed315-117">-WhatIf</span></span>
<span data-ttu-id="ed315-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed315-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed315-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed315-120">CommonParameters</span></span>
<span data-ttu-id="ed315-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed315-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed315-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed315-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed315-123">입력</span><span class="sxs-lookup"><span data-stu-id="ed315-123">INPUTS</span></span>

### <span data-ttu-id="ed315-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ed315-125">출력</span><span class="sxs-lookup"><span data-stu-id="ed315-125">OUTPUTS</span></span>

### <span data-ttu-id="ed315-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ed315-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed315-127">NOTES</span></span>

## <span data-ttu-id="ed315-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed315-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed315-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ed315-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ed315-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ed315-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
