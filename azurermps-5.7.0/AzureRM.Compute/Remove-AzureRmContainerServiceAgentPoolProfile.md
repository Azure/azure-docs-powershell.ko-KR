---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702165"
---
# <span data-ttu-id="a7c7f-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a7c7f-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="a7c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c7f-103">컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7c7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7c7f-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c7f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c7f-106">**제거-AzureRmContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스에서 에이전트 풀 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="a7c7f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7c7f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7c7f-108">예제 1: 컨테이너 서비스에서 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="a7c7f-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="a7c7f-109">첫 번째 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="a7c7f-110">명령이 $Container 변수에 서비스를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="a7c7f-111">두 번째 명령은 $Container에서 컨테이너 서비스의 AgentPool01 이라는 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="a7c7f-112">변수</span><span class="sxs-lookup"><span data-stu-id="a7c7f-112">PARAMETERS</span></span>

### <span data-ttu-id="a7c7f-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="a7c7f-113">-ContainerService</span></span>
<span data-ttu-id="a7c7f-114">이 cmdlet에서 에이전트 풀 프로필을 제거 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c7f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a7c7f-115">-Name</span></span>
<span data-ttu-id="a7c7f-116">이 cmdlet이 제거 하는 에이전트 풀 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7c7f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="a7c7f-117">-Confirm</span></span>
<span data-ttu-id="a7c7f-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c7f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c7f-119">-WhatIf</span></span>
<span data-ttu-id="a7c7f-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7c7f-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c7f-122">CommonParameters</span></span>
<span data-ttu-id="a7c7f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c7f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c7f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c7f-125">입력</span><span class="sxs-lookup"><span data-stu-id="a7c7f-125">INPUTS</span></span>

### <span data-ttu-id="a7c7f-126">않아야</span><span class="sxs-lookup"><span data-stu-id="a7c7f-126">None</span></span>
<span data-ttu-id="a7c7f-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7c7f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7c7f-128">출력</span><span class="sxs-lookup"><span data-stu-id="a7c7f-128">OUTPUTS</span></span>

## <span data-ttu-id="a7c7f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a7c7f-129">NOTES</span></span>

## <span data-ttu-id="a7c7f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7c7f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7c7f-131">추가-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="a7c7f-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="a7c7f-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a7c7f-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


