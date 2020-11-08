---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215590"
---
# <span data-ttu-id="1dc17-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1dc17-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="1dc17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc17-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc17-103">Azure 컨테이너 레지스트리에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="1dc17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dc17-104">SYNTAX</span></span>

### <span data-ttu-id="1dc17-105">WithoutNameAndPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1dc17-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc17-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc17-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc17-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1dc17-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc17-108">Azure 컨테이너 레지스트리에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="1dc17-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1dc17-109">EXAMPLES</span></span>

### <span data-ttu-id="1dc17-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dc17-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="1dc17-111">이미 azure 계정에 로그인 하는 경우 자격 증명이 없는 ACR에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="1dc17-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1dc17-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="1dc17-113">관리자 사용자가 사용 하도록 설정 된 경우 관리자 사용자 이름/암호를 사용 하 여 ACR에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="1dc17-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="1dc17-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="1dc17-115">서비스 사용자 응용 프로그램 ID 및 암호를 사용 하 여 ACR에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="1dc17-116">변수</span><span class="sxs-lookup"><span data-stu-id="1dc17-116">PARAMETERS</span></span>

### <span data-ttu-id="1dc17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc17-117">-DefaultProfile</span></span>
<span data-ttu-id="1dc17-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc17-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1dc17-119">-Name</span></span>
<span data-ttu-id="1dc17-120">Azure 컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="1dc17-121">-암호</span><span class="sxs-lookup"><span data-stu-id="1dc17-121">-Password</span></span>
<span data-ttu-id="1dc17-122">Azure 컨테이너 레지스트리의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="1dc17-123">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="1dc17-123">-UserName</span></span>
<span data-ttu-id="1dc17-124">Azure 컨테이너 레지스트리의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="1dc17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc17-125">CommonParameters</span></span>
<span data-ttu-id="1dc17-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dc17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc17-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1dc17-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc17-128">입력</span><span class="sxs-lookup"><span data-stu-id="1dc17-128">INPUTS</span></span>

### <span data-ttu-id="1dc17-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1dc17-129">System.String</span></span>

## <span data-ttu-id="1dc17-130">출력</span><span class="sxs-lookup"><span data-stu-id="1dc17-130">OUTPUTS</span></span>

### <span data-ttu-id="1dc17-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1dc17-131">System.Boolean</span></span>

## <span data-ttu-id="1dc17-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1dc17-132">NOTES</span></span>

## <span data-ttu-id="1dc17-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dc17-133">RELATED LINKS</span></span>
