---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953792"
---
# <span data-ttu-id="50231-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="50231-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="50231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50231-102">SYNOPSIS</span></span>
<span data-ttu-id="50231-103">서비스 엔드포인트 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50231-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="50231-104">구문</span><span class="sxs-lookup"><span data-stu-id="50231-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50231-105">설명</span><span class="sxs-lookup"><span data-stu-id="50231-105">DESCRIPTION</span></span>
<span data-ttu-id="50231-106">**New-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="50231-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="50231-107">예제</span><span class="sxs-lookup"><span data-stu-id="50231-107">EXAMPLES</span></span>

### <span data-ttu-id="50231-108">예제 1: 서비스 엔드포인트 정책 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50231-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="50231-109">이 명령은 개체가 정의한 정의가 있는 Policy1이라는 서비스 엔드포인트 정책을 $serviceEndpointDefinition 정의를 만들고 $serviceEndpointPolicy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="50231-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="50231-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50231-110">PARAMETERS</span></span>

### <span data-ttu-id="50231-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50231-111">-DefaultProfile</span></span>
<span data-ttu-id="50231-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50231-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50231-113">-Force</span><span class="sxs-lookup"><span data-stu-id="50231-113">-Force</span></span>
<span data-ttu-id="50231-114">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50231-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="50231-115">-Location</span><span class="sxs-lookup"><span data-stu-id="50231-115">-Location</span></span>
<span data-ttu-id="50231-116">위치.</span><span class="sxs-lookup"><span data-stu-id="50231-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50231-117">-Name</span><span class="sxs-lookup"><span data-stu-id="50231-117">-Name</span></span>
<span data-ttu-id="50231-118">서브넷의 이름</span><span class="sxs-lookup"><span data-stu-id="50231-118">The name of the subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50231-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50231-119">-ResourceGroupName</span></span>
<span data-ttu-id="50231-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50231-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50231-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="50231-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="50231-122">서비스 엔드포인트 정의 목록</span><span class="sxs-lookup"><span data-stu-id="50231-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50231-123">-확인</span><span class="sxs-lookup"><span data-stu-id="50231-123">-Confirm</span></span>
<span data-ttu-id="50231-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50231-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50231-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50231-125">-WhatIf</span></span>
<span data-ttu-id="50231-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50231-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50231-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50231-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50231-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50231-128">CommonParameters</span></span>
<span data-ttu-id="50231-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50231-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50231-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50231-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50231-131">입력</span><span class="sxs-lookup"><span data-stu-id="50231-131">INPUTS</span></span>

### <span data-ttu-id="50231-132">System.String</span><span class="sxs-lookup"><span data-stu-id="50231-132">System.String</span></span>

## <span data-ttu-id="50231-133">출력</span><span class="sxs-lookup"><span data-stu-id="50231-133">OUTPUTS</span></span>

### <span data-ttu-id="50231-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="50231-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="50231-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50231-135">NOTES</span></span>

## <span data-ttu-id="50231-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50231-136">RELATED LINKS</span></span>

[<span data-ttu-id="50231-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="50231-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="50231-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="50231-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="50231-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="50231-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
