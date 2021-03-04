---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 71eb25c99197513bead7cb400b8a5648c137442d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956304"
---
# <span data-ttu-id="bfa10-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bfa10-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="bfa10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa10-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa10-103">컨테이너 레지스트리에 대한 로그인 자격 증명을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="bfa10-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfa10-104">SYNTAX</span></span>

### <span data-ttu-id="bfa10-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bfa10-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa10-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfa10-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfa10-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfa10-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa10-108">설명</span><span class="sxs-lookup"><span data-stu-id="bfa10-108">DESCRIPTION</span></span>
<span data-ttu-id="bfa10-109">Update-AzContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대한 로그인 자격 증명을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="bfa10-110">예제</span><span class="sxs-lookup"><span data-stu-id="bfa10-110">EXAMPLES</span></span>

### <span data-ttu-id="bfa10-111">예제 1: 컨테이너 레지스트리에 대한 로그인 자격 증명 다시 생성</span><span class="sxs-lookup"><span data-stu-id="bfa10-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="bfa10-112">이 명령은 지정된 컨테이너 레지스트리에 대한 로그인 자격 증명을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="bfa10-113">관리 사용자는 컨테이너 레지스트리 MyRegistry에서 로그인 자격 증명을 다시 생성하도록 \` \` 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="bfa10-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfa10-114">PARAMETERS</span></span>

### <span data-ttu-id="bfa10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa10-115">-DefaultProfile</span></span>
<span data-ttu-id="bfa10-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bfa10-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfa10-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bfa10-117">-Name</span></span>
<span data-ttu-id="bfa10-118">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa10-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="bfa10-119">-PasswordName</span></span>
<span data-ttu-id="bfa10-120">다시 생성할 암호의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-120">The name of password to regenerate.</span></span>
<span data-ttu-id="bfa10-121">허용되는 값: 암호, 암호2.</span><span class="sxs-lookup"><span data-stu-id="bfa10-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa10-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="bfa10-122">-Registry</span></span>
<span data-ttu-id="bfa10-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa10-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfa10-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa10-126">-ResourceId</span></span>
<span data-ttu-id="bfa10-127">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bfa10-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa10-128">-확인</span><span class="sxs-lookup"><span data-stu-id="bfa10-128">-Confirm</span></span>
<span data-ttu-id="bfa10-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa10-130">-WhatIf</span></span>
<span data-ttu-id="bfa10-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa10-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa10-133">CommonParameters</span></span>
<span data-ttu-id="bfa10-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfa10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa10-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfa10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa10-136">입력</span><span class="sxs-lookup"><span data-stu-id="bfa10-136">INPUTS</span></span>

### <span data-ttu-id="bfa10-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bfa10-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="bfa10-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bfa10-138">System.String</span></span>

## <span data-ttu-id="bfa10-139">출력</span><span class="sxs-lookup"><span data-stu-id="bfa10-139">OUTPUTS</span></span>

### <span data-ttu-id="bfa10-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bfa10-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="bfa10-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfa10-141">NOTES</span></span>

## <span data-ttu-id="bfa10-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfa10-142">RELATED LINKS</span></span>

[<span data-ttu-id="bfa10-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bfa10-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="bfa10-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bfa10-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="bfa10-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bfa10-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

