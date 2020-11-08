---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056489"
---
# <span data-ttu-id="5a10c-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5a10c-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="5a10c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a10c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a10c-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="5a10c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a10c-104">SYNTAX</span></span>

### <span data-ttu-id="5a10c-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a10c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a10c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a10c-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a10c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a10c-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a10c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a10c-108">DESCRIPTION</span></span>
<span data-ttu-id="5a10c-109">Get-AzContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="5a10c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a10c-110">EXAMPLES</span></span>

### <span data-ttu-id="5a10c-111">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a10c-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="5a10c-112">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="5a10c-113">\`로그인 자격 증명을 얻으려면 컨테이너 레지스트리 myregistry에 대해 관리자 사용자가 사용 하도록 설정 되어 있어야 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="5a10c-114">변수</span><span class="sxs-lookup"><span data-stu-id="5a10c-114">PARAMETERS</span></span>

### <span data-ttu-id="5a10c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a10c-115">-DefaultProfile</span></span>
<span data-ttu-id="5a10c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a10c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a10c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5a10c-117">-Name</span></span>
<span data-ttu-id="5a10c-118">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="5a10c-119">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="5a10c-119">-Registry</span></span>
<span data-ttu-id="5a10c-120">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="5a10c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a10c-121">-ResourceGroupName</span></span>
<span data-ttu-id="5a10c-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="5a10c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a10c-123">-ResourceId</span></span>
<span data-ttu-id="5a10c-124">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="5a10c-124">The container registry resource id</span></span>

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

### <span data-ttu-id="5a10c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a10c-125">CommonParameters</span></span>
<span data-ttu-id="5a10c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a10c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a10c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a10c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a10c-128">입력</span><span class="sxs-lookup"><span data-stu-id="5a10c-128">INPUTS</span></span>

### <span data-ttu-id="5a10c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a10c-129">System.String</span></span>

## <span data-ttu-id="5a10c-130">출력</span><span class="sxs-lookup"><span data-stu-id="5a10c-130">OUTPUTS</span></span>

### <span data-ttu-id="5a10c-131">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5a10c-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="5a10c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5a10c-132">NOTES</span></span>

## <span data-ttu-id="5a10c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a10c-133">RELATED LINKS</span></span>

[<span data-ttu-id="5a10c-134">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5a10c-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="5a10c-135">업데이트-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5a10c-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="5a10c-136">업데이트-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5a10c-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

