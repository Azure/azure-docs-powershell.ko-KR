---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344678"
---
# <span data-ttu-id="d5274-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d5274-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="d5274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5274-102">SYNOPSIS</span></span>
<span data-ttu-id="d5274-103">Azure Container Registry에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="d5274-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5274-104">SYNTAX</span></span>

### <span data-ttu-id="d5274-105">WithoutNameAndPasswordParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5274-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5274-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5274-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5274-107">설명</span><span class="sxs-lookup"><span data-stu-id="d5274-107">DESCRIPTION</span></span>
<span data-ttu-id="d5274-108">Azure Container Registry에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="d5274-109">예제</span><span class="sxs-lookup"><span data-stu-id="d5274-109">EXAMPLES</span></span>

### <span data-ttu-id="d5274-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5274-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="d5274-111">Azure 계정에 이미 로그인한 경우 자격 증명이 없는 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="d5274-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d5274-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="d5274-113">관리 사용자를 사용하도록 설정한 경우 관리자 사용자 이름/암호를 사용하여 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="d5274-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="d5274-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="d5274-115">서비스 주체 애플리케이션 ID 및 암호를 사용하여 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="d5274-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5274-116">PARAMETERS</span></span>

### <span data-ttu-id="d5274-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5274-117">-DefaultProfile</span></span>
<span data-ttu-id="d5274-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5274-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d5274-119">-Name</span></span>
<span data-ttu-id="d5274-120">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5274-121">-Password</span><span class="sxs-lookup"><span data-stu-id="d5274-121">-Password</span></span>
<span data-ttu-id="d5274-122">Azure Container Registry에 대한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5274-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="d5274-123">-UserName</span></span>
<span data-ttu-id="d5274-124">Azure Container Registry의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5274-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5274-125">CommonParameters</span></span>
<span data-ttu-id="d5274-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5274-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5274-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5274-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5274-128">입력</span><span class="sxs-lookup"><span data-stu-id="d5274-128">INPUTS</span></span>

### <span data-ttu-id="d5274-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5274-129">System.String</span></span>

## <span data-ttu-id="d5274-130">출력</span><span class="sxs-lookup"><span data-stu-id="d5274-130">OUTPUTS</span></span>

### <span data-ttu-id="d5274-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5274-131">System.Boolean</span></span>

## <span data-ttu-id="d5274-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5274-132">NOTES</span></span>

## <span data-ttu-id="d5274-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5274-133">RELATED LINKS</span></span>
