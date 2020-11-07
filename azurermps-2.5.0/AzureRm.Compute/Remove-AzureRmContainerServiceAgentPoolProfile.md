---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882321"
---
# <span data-ttu-id="cb629-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cb629-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="cb629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb629-102">SYNOPSIS</span></span>
<span data-ttu-id="cb629-103">컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb629-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb629-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb629-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb629-105">DESCRIPTION</span></span>
<span data-ttu-id="cb629-106">**제거-AzureRmContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="cb629-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cb629-107">EXAMPLES</span></span>

### <span data-ttu-id="cb629-108">예제 1: 컨테이너 서비스에서 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="cb629-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="cb629-109">첫 번째 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="cb629-110">명령이 $Container 변수에 서비스를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="cb629-111">두 번째 명령은 $Container에서 컨테이너 서비스의 AgentPool01 이라는 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="cb629-112">변수</span><span class="sxs-lookup"><span data-stu-id="cb629-112">PARAMETERS</span></span>

### <span data-ttu-id="cb629-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="cb629-113">-ContainerService</span></span>
<span data-ttu-id="cb629-114">이 cmdlet에서 에이전트 풀 프로필을 제거 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb629-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb629-115">-DefaultProfile</span></span>
<span data-ttu-id="cb629-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb629-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cb629-117">-Name</span></span>
<span data-ttu-id="cb629-118">이 cmdlet이 제거 하는 에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cb629-119">-확인</span><span class="sxs-lookup"><span data-stu-id="cb629-119">-Confirm</span></span>
<span data-ttu-id="cb629-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb629-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb629-121">-WhatIf</span></span>
<span data-ttu-id="cb629-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb629-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb629-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb629-124">CommonParameters</span></span>
<span data-ttu-id="cb629-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb629-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb629-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb629-127">입력</span><span class="sxs-lookup"><span data-stu-id="cb629-127">INPUTS</span></span>

### <span data-ttu-id="cb629-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="cb629-128">ContainerService</span></span>
<span data-ttu-id="cb629-129">' ContainerService ' 매개 변수는 파이프라인에서 ' ContainerService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb629-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="cb629-130">출력</span><span class="sxs-lookup"><span data-stu-id="cb629-130">OUTPUTS</span></span>

### <span data-ttu-id="cb629-131">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="cb629-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="cb629-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cb629-132">NOTES</span></span>

## <span data-ttu-id="cb629-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb629-133">RELATED LINKS</span></span>

[<span data-ttu-id="cb629-134">추가-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cb629-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="cb629-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cb629-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


