---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 086085bd1a36c1508cf489d224ddd6bff4651c50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701206"
---
# <span data-ttu-id="f19fc-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f19fc-101">Update-AzContainerService</span></span>

## <span data-ttu-id="f19fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f19fc-103">컨테이너 서비스의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="f19fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f19fc-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f19fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f19fc-106">**업데이트 AzContainerService** cmdlet은 서비스의 로컬 인스턴스와 일치 하도록 컨테이너 서비스의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="f19fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f19fc-107">EXAMPLES</span></span>

### <span data-ttu-id="f19fc-108">예제 1: 컨테이너 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="f19fc-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="f19fc-109">이 명령은 Get-AzContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="f19fc-110">이 명령은 파이프라인 연산자를 사용 하 여 Remove-AzContainerServiceAgentPoolProfile cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f19fc-111">**제거-AzContainerServiceAgentPoolProfile** 는 AgentPool01 이라는 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="f19fc-112">명령이 결과를 Add-AzContainerServiceAgentPoolProfile cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="f19fc-113">**추가-AzContainerServiceAgentPoolProfile** 이름이 AgentPool01이 고 지정 된 속성이 있는 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="f19fc-114">명령이 결과를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="f19fc-115">현재 cmdlet은이 명령에 대 한 변경 내용을 반영 하도록 컨테이너 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="f19fc-116">변수</span><span class="sxs-lookup"><span data-stu-id="f19fc-116">PARAMETERS</span></span>

### <span data-ttu-id="f19fc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f19fc-117">-AsJob</span></span>
<span data-ttu-id="f19fc-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f19fc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f19fc-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f19fc-119">-ContainerService</span></span>
<span data-ttu-id="f19fc-120">변경 내용이 포함 된 로컬 **ContainerService** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f19fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19fc-121">-DefaultProfile</span></span>
<span data-ttu-id="f19fc-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f19fc-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f19fc-123">-Name</span></span>
<span data-ttu-id="f19fc-124">이 cmdlet이 업데이트 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f19fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="f19fc-126">이 cmdlet이 업데이트 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f19fc-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f19fc-127">-Confirm</span></span>
<span data-ttu-id="f19fc-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19fc-129">-WhatIf</span></span>
<span data-ttu-id="f19fc-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19fc-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19fc-132">CommonParameters</span></span>
<span data-ttu-id="f19fc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f19fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19fc-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19fc-135">입력</span><span class="sxs-lookup"><span data-stu-id="f19fc-135">INPUTS</span></span>

### <span data-ttu-id="f19fc-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f19fc-136">System.String</span></span>

### <span data-ttu-id="f19fc-137">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="f19fc-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f19fc-138">출력</span><span class="sxs-lookup"><span data-stu-id="f19fc-138">OUTPUTS</span></span>

### <span data-ttu-id="f19fc-139">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="f19fc-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f19fc-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f19fc-140">NOTES</span></span>

## <span data-ttu-id="f19fc-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f19fc-141">RELATED LINKS</span></span>

[<span data-ttu-id="f19fc-142">추가-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f19fc-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f19fc-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f19fc-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="f19fc-144">새로운 AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f19fc-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="f19fc-145">제거-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f19fc-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="f19fc-146">제거-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f19fc-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


