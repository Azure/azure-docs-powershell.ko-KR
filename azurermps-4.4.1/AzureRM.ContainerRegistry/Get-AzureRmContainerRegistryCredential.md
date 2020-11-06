---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531822"
---
# <span data-ttu-id="4ed23-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4ed23-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="4ed23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed23-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed23-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ed23-104">SYNTAX</span></span>

### <span data-ttu-id="4ed23-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ed23-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed23-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed23-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed23-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ed23-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed23-108">**Get-AzureRmContainerRegistryCredential** cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="4ed23-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4ed23-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed23-110">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ed23-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="4ed23-111">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="4ed23-112">로그인 자격 증명을 얻으려면 컨테이너 레지스트리에 대 한 관리자 사용자가 설정 되어 있어야 `MyRegistry` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="4ed23-113">변수</span><span class="sxs-lookup"><span data-stu-id="4ed23-113">PARAMETERS</span></span>

### <span data-ttu-id="4ed23-114">-이름</span><span class="sxs-lookup"><span data-stu-id="4ed23-114">-Name</span></span>
<span data-ttu-id="4ed23-115">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="4ed23-116">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="4ed23-116">-Registry</span></span>
<span data-ttu-id="4ed23-117">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-117">Container Registry Object.</span></span>

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

### <span data-ttu-id="4ed23-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed23-118">-ResourceGroupName</span></span>
<span data-ttu-id="4ed23-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="4ed23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed23-120">-DefaultProfile</span></span>
<span data-ttu-id="4ed23-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed23-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed23-122">CommonParameters</span></span>
<span data-ttu-id="4ed23-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed23-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed23-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed23-125">입력</span><span class="sxs-lookup"><span data-stu-id="4ed23-125">INPUTS</span></span>

### <span data-ttu-id="4ed23-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4ed23-126">PSContainerRegistry</span></span>
<span data-ttu-id="4ed23-127">' Registry ' 매개 변수는 파이프라인에서 ' PSContainerRegistry ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ed23-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="4ed23-128">출력</span><span class="sxs-lookup"><span data-stu-id="4ed23-128">OUTPUTS</span></span>

### <span data-ttu-id="4ed23-129">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4ed23-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="4ed23-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4ed23-130">NOTES</span></span>

## <span data-ttu-id="4ed23-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ed23-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ed23-132">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4ed23-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="4ed23-133">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4ed23-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="4ed23-134">업데이트-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4ed23-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

