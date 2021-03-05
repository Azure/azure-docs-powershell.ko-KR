---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 5e20ae556cba16263d8b650de869b174236ccbd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004427"
---
# <span data-ttu-id="e909e-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e909e-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="e909e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e909e-102">SYNOPSIS</span></span>
<span data-ttu-id="e909e-103">컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e909e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e909e-104">SYNTAX</span></span>

### <span data-ttu-id="e909e-105">NameResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e909e-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e909e-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e909e-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e909e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e909e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e909e-108">설명</span><span class="sxs-lookup"><span data-stu-id="e909e-108">DESCRIPTION</span></span>
<span data-ttu-id="e909e-109">Get-AzContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e909e-110">예제</span><span class="sxs-lookup"><span data-stu-id="e909e-110">EXAMPLES</span></span>

### <span data-ttu-id="e909e-111">예제 1: 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="e909e-112">이 명령은 지정된 컨테이너 레지스트리에 대한 로그인 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="e909e-113">관리자 사용자는 로그인 자격 증명을 얻기 위해 컨테이너 레지스트리 \` MyRegistry에 사용하도록 \` 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="e909e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e909e-114">PARAMETERS</span></span>

### <span data-ttu-id="e909e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e909e-115">-DefaultProfile</span></span>
<span data-ttu-id="e909e-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e909e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e909e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e909e-117">-Name</span></span>
<span data-ttu-id="e909e-118">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="e909e-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="e909e-119">-Registry</span></span>
<span data-ttu-id="e909e-120">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="e909e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e909e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e909e-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e909e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e909e-123">-ResourceId</span></span>
<span data-ttu-id="e909e-124">컨테이너 레지스트리 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e909e-124">The container registry resource id</span></span>

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

### <span data-ttu-id="e909e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e909e-125">CommonParameters</span></span>
<span data-ttu-id="e909e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e909e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e909e-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e909e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e909e-128">입력</span><span class="sxs-lookup"><span data-stu-id="e909e-128">INPUTS</span></span>

### <span data-ttu-id="e909e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e909e-129">System.String</span></span>

## <span data-ttu-id="e909e-130">출력</span><span class="sxs-lookup"><span data-stu-id="e909e-130">OUTPUTS</span></span>

### <span data-ttu-id="e909e-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e909e-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="e909e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e909e-132">NOTES</span></span>

## <span data-ttu-id="e909e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e909e-133">RELATED LINKS</span></span>

[<span data-ttu-id="e909e-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e909e-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e909e-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e909e-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="e909e-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e909e-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

