---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: bacc9366292225e07fd07ac65726018f1d1879e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526224"
---
# <span data-ttu-id="dd1c2-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="dd1c2-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="dd1c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1c2-103">컨테이너 서비스의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd1c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd1c2-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd1c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd1c2-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1c2-106">**업데이트 AzureRmContainerService** cmdlet은 서비스의 로컬 인스턴스와 일치 하도록 컨테이너 서비스의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="dd1c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dd1c2-107">EXAMPLES</span></span>

### <span data-ttu-id="dd1c2-108">예제 1: 컨테이너 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="dd1c2-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="dd1c2-109">이 명령은 Get-AzureRmContainerService cmdlet을 사용 하 여 CSResourceGroup17 이라는 컨테이너 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="dd1c2-110">이 명령은 파이프라인 연산자를 사용 하 여 Remove-AzureRmContainerServiceAgentPoolProfile cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dd1c2-111">**제거-AzureRmContainerServiceAgentPoolProfile** 는 AgentPool01 이라는 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="dd1c2-112">명령이 결과를 Add-AzureRmContainerServiceAgentPoolProfile cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="dd1c2-113">**추가-AzureRmContainerServiceAgentPoolProfile** 이름이 AgentPool01이 고 지정 된 속성이 있는 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="dd1c2-114">명령이 결과를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="dd1c2-115">현재 cmdlet은이 명령에 대 한 변경 내용을 반영 하도록 컨테이너 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="dd1c2-116">변수</span><span class="sxs-lookup"><span data-stu-id="dd1c2-116">PARAMETERS</span></span>

### <span data-ttu-id="dd1c2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd1c2-117">-AsJob</span></span>
<span data-ttu-id="dd1c2-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dd1c2-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd1c2-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="dd1c2-119">-ContainerService</span></span>
<span data-ttu-id="dd1c2-120">변경 내용이 포함 된 로컬 **ContainerService** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c2-121">-DefaultProfile</span></span>
<span data-ttu-id="dd1c2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd1c2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="dd1c2-123">-Name</span></span>
<span data-ttu-id="dd1c2-124">이 cmdlet이 업데이트 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd1c2-126">이 cmdlet이 업데이트 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="dd1c2-127">-확인</span><span class="sxs-lookup"><span data-stu-id="dd1c2-127">-Confirm</span></span>
<span data-ttu-id="dd1c2-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd1c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1c2-129">-WhatIf</span></span>
<span data-ttu-id="dd1c2-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1c2-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd1c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1c2-132">CommonParameters</span></span>
<span data-ttu-id="dd1c2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1c2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1c2-135">입력</span><span class="sxs-lookup"><span data-stu-id="dd1c2-135">INPUTS</span></span>

### <span data-ttu-id="dd1c2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd1c2-136">System.String</span></span>

### <span data-ttu-id="dd1c2-137">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="dd1c2-138">매개 변수: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd1c2-138">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="dd1c2-139">출력</span><span class="sxs-lookup"><span data-stu-id="dd1c2-139">OUTPUTS</span></span>

### <span data-ttu-id="dd1c2-140">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="dd1c2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="dd1c2-141">NOTES</span></span>

## <span data-ttu-id="dd1c2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd1c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd1c2-143">추가-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c2-143">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="dd1c2-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="dd1c2-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="dd1c2-145">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="dd1c2-145">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="dd1c2-146">제거-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="dd1c2-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="dd1c2-147">제거-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c2-147">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


