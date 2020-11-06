---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534239"
---
# <span data-ttu-id="0e2c2-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e2c2-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="0e2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2c2-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="0e2c2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e2c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e2c2-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e2c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="0e2c2-106">**새 AzureRmServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="0e2c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e2c2-107">EXAMPLES</span></span>

### <span data-ttu-id="0e2c2-108">예제 1: 서비스 끝점 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0e2c2-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="0e2c2-109">이 명령은 개체 $serviceEndpointDefinition 정의 하는 정의를 사용 하 여 Policy1 라는 서비스 끝점 정책을 만들고이를 $serviceEndpointPolicy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="0e2c2-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e2c2-110">PARAMETERS</span></span>

### <span data-ttu-id="0e2c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2c2-111">-DefaultProfile</span></span>
<span data-ttu-id="0e2c2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e2c2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0e2c2-113">-Force</span></span>
<span data-ttu-id="0e2c2-114">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="0e2c2-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0e2c2-115">-Name</span></span>
<span data-ttu-id="0e2c2-116">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e2c2-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="0e2c2-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="0e2c2-120">서비스 끝점 정의 목록</span><span class="sxs-lookup"><span data-stu-id="0e2c2-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0e2c2-121">-Confirm</span></span>
<span data-ttu-id="0e2c2-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2c2-123">-WhatIf</span></span>
<span data-ttu-id="0e2c2-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e2c2-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2c2-126">CommonParameters</span></span>
<span data-ttu-id="0e2c2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e2c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0e2c2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e2c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2c2-129">입력</span><span class="sxs-lookup"><span data-stu-id="0e2c2-129">INPUTS</span></span>

### <span data-ttu-id="0e2c2-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e2c2-130">System.String</span></span>


## <span data-ttu-id="0e2c2-131">출력</span><span class="sxs-lookup"><span data-stu-id="0e2c2-131">OUTPUTS</span></span>

### <span data-ttu-id="0e2c2-132">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0e2c2-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="0e2c2-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0e2c2-133">NOTES</span></span>

## <span data-ttu-id="0e2c2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e2c2-134">RELATED LINKS</span></span>
