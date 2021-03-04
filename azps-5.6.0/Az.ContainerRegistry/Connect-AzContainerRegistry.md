---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004459"
---
# <span data-ttu-id="1ced9-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1ced9-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="1ced9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ced9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ced9-103">Azure 컨테이너 레지스트리에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="1ced9-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ced9-104">SYNTAX</span></span>

### <span data-ttu-id="1ced9-105">WithoutNameAndPasswordParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ced9-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ced9-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ced9-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ced9-107">설명</span><span class="sxs-lookup"><span data-stu-id="1ced9-107">DESCRIPTION</span></span>
<span data-ttu-id="1ced9-108">Azure 컨테이너 레지스트리에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="1ced9-109">예제</span><span class="sxs-lookup"><span data-stu-id="1ced9-109">EXAMPLES</span></span>

### <span data-ttu-id="1ced9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ced9-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="1ced9-111">Azure 계정에 이미 로그인할 때 자격 증명이 없는 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="1ced9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1ced9-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="1ced9-113">관리자 사용자를 사용하도록 설정한 경우 관리자 사용자 이름/암호를 사용하여 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="1ced9-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="1ced9-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="1ced9-115">서비스 주체 애플리케이션 ID 및 암호를 사용하여 ACR에 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="1ced9-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ced9-116">PARAMETERS</span></span>

### <span data-ttu-id="1ced9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ced9-117">-DefaultProfile</span></span>
<span data-ttu-id="1ced9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ced9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1ced9-119">-Name</span></span>
<span data-ttu-id="1ced9-120">Azure Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ced9-121">-Password</span><span class="sxs-lookup"><span data-stu-id="1ced9-121">-Password</span></span>
<span data-ttu-id="1ced9-122">Azure Container Registry의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="1ced9-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="1ced9-123">-UserName</span></span>
<span data-ttu-id="1ced9-124">Azure Container Registry의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="1ced9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ced9-125">CommonParameters</span></span>
<span data-ttu-id="1ced9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ced9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ced9-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ced9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ced9-128">입력</span><span class="sxs-lookup"><span data-stu-id="1ced9-128">INPUTS</span></span>

### <span data-ttu-id="1ced9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1ced9-129">System.String</span></span>

## <span data-ttu-id="1ced9-130">출력</span><span class="sxs-lookup"><span data-stu-id="1ced9-130">OUTPUTS</span></span>

### <span data-ttu-id="1ced9-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ced9-131">System.Boolean</span></span>

## <span data-ttu-id="1ced9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ced9-132">NOTES</span></span>

## <span data-ttu-id="1ced9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ced9-133">RELATED LINKS</span></span>
