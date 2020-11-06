---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536683"
---
# <span data-ttu-id="65fdb-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="65fdb-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="65fdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="65fdb-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65fdb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65fdb-104">SYNTAX</span></span>

### <span data-ttu-id="65fdb-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="65fdb-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65fdb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fdb-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fdb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65fdb-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fdb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="65fdb-108">DESCRIPTION</span></span>
<span data-ttu-id="65fdb-109">Update-AzureRmContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="65fdb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65fdb-110">EXAMPLES</span></span>

### <span data-ttu-id="65fdb-111">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 다시 생성</span><span class="sxs-lookup"><span data-stu-id="65fdb-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="65fdb-112">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="65fdb-113">\` \` 로그인 자격 증명을 다시 생성 하기 위해 관리 사용자에 게 컨테이너 레지스트리 myregistry을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="65fdb-114">변수</span><span class="sxs-lookup"><span data-stu-id="65fdb-114">PARAMETERS</span></span>

### <span data-ttu-id="65fdb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fdb-115">-DefaultProfile</span></span>
<span data-ttu-id="65fdb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65fdb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65fdb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="65fdb-117">-Name</span></span>
<span data-ttu-id="65fdb-118">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="65fdb-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="65fdb-119">-PasswordName</span></span>
<span data-ttu-id="65fdb-120">다시 생성할 암호의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-120">The name of password to regenerate.</span></span>
<span data-ttu-id="65fdb-121">허용 되는 값: password, password2.</span><span class="sxs-lookup"><span data-stu-id="65fdb-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="65fdb-122">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="65fdb-122">-Registry</span></span>
<span data-ttu-id="65fdb-123">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="65fdb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fdb-124">-ResourceGroupName</span></span>
<span data-ttu-id="65fdb-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="65fdb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65fdb-126">-ResourceId</span></span>
<span data-ttu-id="65fdb-127">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="65fdb-127">The container registry resource id</span></span>

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

### <span data-ttu-id="65fdb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="65fdb-128">-Confirm</span></span>
<span data-ttu-id="65fdb-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fdb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fdb-130">-WhatIf</span></span>
<span data-ttu-id="65fdb-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65fdb-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fdb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fdb-133">CommonParameters</span></span>
<span data-ttu-id="65fdb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fdb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fdb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65fdb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fdb-136">입력</span><span class="sxs-lookup"><span data-stu-id="65fdb-136">INPUTS</span></span>

### <span data-ttu-id="65fdb-137">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65fdb-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="65fdb-138">매개 변수: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65fdb-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="65fdb-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65fdb-139">System.String</span></span>

## <span data-ttu-id="65fdb-140">출력</span><span class="sxs-lookup"><span data-stu-id="65fdb-140">OUTPUTS</span></span>

### <span data-ttu-id="65fdb-141">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="65fdb-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="65fdb-142">상속자</span><span class="sxs-lookup"><span data-stu-id="65fdb-142">NOTES</span></span>

## <span data-ttu-id="65fdb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65fdb-143">RELATED LINKS</span></span>

[<span data-ttu-id="65fdb-144">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65fdb-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="65fdb-145">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65fdb-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="65fdb-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="65fdb-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

