---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351218"
---
# <span data-ttu-id="dd5e2-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="dd5e2-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="dd5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5e2-103">컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="dd5e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd5e2-104">SYNTAX</span></span>

### <span data-ttu-id="dd5e2-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd5e2-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd5e2-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd5e2-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd5e2-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd5e2-108">설명</span><span class="sxs-lookup"><span data-stu-id="dd5e2-108">DESCRIPTION</span></span>
<span data-ttu-id="dd5e2-109">Get-AzContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="dd5e2-110">예제</span><span class="sxs-lookup"><span data-stu-id="dd5e2-110">EXAMPLES</span></span>

### <span data-ttu-id="dd5e2-111">예제 1: 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="dd5e2-112">이 명령은 지정된 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="dd5e2-113">로그인 자격 증명을 얻기 위해 컨테이너 레지스트리 MyRegistry에 대해 관리 사용자를 사용하도록 \` \` 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="dd5e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd5e2-114">PARAMETERS</span></span>

### <span data-ttu-id="dd5e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5e2-115">-DefaultProfile</span></span>
<span data-ttu-id="dd5e2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dd5e2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd5e2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dd5e2-117">-Name</span></span>
<span data-ttu-id="dd5e2-118">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="dd5e2-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="dd5e2-119">-Registry</span></span>
<span data-ttu-id="dd5e2-120">Container Registry 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd5e2-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd5e2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5e2-123">-ResourceId</span></span>
<span data-ttu-id="dd5e2-124">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dd5e2-124">The container registry resource id</span></span>

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

### <span data-ttu-id="dd5e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5e2-125">CommonParameters</span></span>
<span data-ttu-id="dd5e2-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5e2-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd5e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5e2-128">입력</span><span class="sxs-lookup"><span data-stu-id="dd5e2-128">INPUTS</span></span>

### <span data-ttu-id="dd5e2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dd5e2-129">System.String</span></span>

## <span data-ttu-id="dd5e2-130">출력</span><span class="sxs-lookup"><span data-stu-id="dd5e2-130">OUTPUTS</span></span>

### <span data-ttu-id="dd5e2-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="dd5e2-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="dd5e2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd5e2-132">NOTES</span></span>

## <span data-ttu-id="dd5e2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd5e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="dd5e2-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd5e2-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="dd5e2-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd5e2-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="dd5e2-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="dd5e2-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

