---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 355938c64926d0c97d7e1393abd5c8a0d5ce20ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536428"
---
# <span data-ttu-id="89b33-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="89b33-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="89b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b33-102">SYNOPSIS</span></span>
<span data-ttu-id="89b33-103">컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89b33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89b33-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b33-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89b33-105">DESCRIPTION</span></span>
<span data-ttu-id="89b33-106">**제거-AzureRmContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="89b33-107">예제의</span><span class="sxs-lookup"><span data-stu-id="89b33-107">EXAMPLES</span></span>

### <span data-ttu-id="89b33-108">예제 1: 컨테이너 서비스에서 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="89b33-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="89b33-109">첫 번째 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="89b33-110">명령이 $Container 변수에 서비스를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="89b33-111">두 번째 명령은 $Container에서 컨테이너 서비스의 AgentPool01 이라는 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="89b33-112">변수</span><span class="sxs-lookup"><span data-stu-id="89b33-112">PARAMETERS</span></span>

### <span data-ttu-id="89b33-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="89b33-113">-ContainerService</span></span>
<span data-ttu-id="89b33-114">이 cmdlet에서 에이전트 풀 프로필을 제거 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b33-115">-DefaultProfile</span></span>
<span data-ttu-id="89b33-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b33-117">-이름</span><span class="sxs-lookup"><span data-stu-id="89b33-117">-Name</span></span>
<span data-ttu-id="89b33-118">이 cmdlet이 제거 하는 에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89b33-119">-확인</span><span class="sxs-lookup"><span data-stu-id="89b33-119">-Confirm</span></span>
<span data-ttu-id="89b33-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b33-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b33-121">-WhatIf</span></span>
<span data-ttu-id="89b33-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89b33-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b33-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b33-124">CommonParameters</span></span>
<span data-ttu-id="89b33-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89b33-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b33-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b33-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b33-127">입력</span><span class="sxs-lookup"><span data-stu-id="89b33-127">INPUTS</span></span>

## <span data-ttu-id="89b33-128">출력</span><span class="sxs-lookup"><span data-stu-id="89b33-128">OUTPUTS</span></span>

## <span data-ttu-id="89b33-129">상속자</span><span class="sxs-lookup"><span data-stu-id="89b33-129">NOTES</span></span>

## <span data-ttu-id="89b33-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89b33-130">RELATED LINKS</span></span>

[<span data-ttu-id="89b33-131">추가-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="89b33-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="89b33-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="89b33-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


