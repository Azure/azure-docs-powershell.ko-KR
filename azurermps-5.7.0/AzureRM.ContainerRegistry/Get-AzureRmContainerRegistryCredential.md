---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536039"
---
# <span data-ttu-id="1dd04-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1dd04-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="1dd04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd04-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd04-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dd04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dd04-104">SYNTAX</span></span>

### <span data-ttu-id="1dd04-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1dd04-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dd04-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd04-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dd04-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd04-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dd04-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1dd04-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd04-109">Get-AzureRmContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="1dd04-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1dd04-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd04-111">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd04-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="1dd04-112">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="1dd04-113">\`로그인 자격 증명을 얻으려면 컨테이너 레지스트리 myregistry에 대해 관리자 사용자가 사용 하도록 설정 되어 있어야 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="1dd04-114">변수</span><span class="sxs-lookup"><span data-stu-id="1dd04-114">PARAMETERS</span></span>

### <span data-ttu-id="1dd04-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1dd04-115">-Name</span></span>
<span data-ttu-id="1dd04-116">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-117">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="1dd04-117">-Registry</span></span>
<span data-ttu-id="1dd04-118">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-118">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd04-119">-ResourceGroupName</span></span>
<span data-ttu-id="1dd04-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd04-121">-DefaultProfile</span></span>
<span data-ttu-id="1dd04-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1dd04-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd04-123">-ResourceId</span></span>
<span data-ttu-id="1dd04-124">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="1dd04-124">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd04-125">CommonParameters</span></span>
<span data-ttu-id="1dd04-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd04-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd04-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd04-128">입력</span><span class="sxs-lookup"><span data-stu-id="1dd04-128">INPUTS</span></span>

### <span data-ttu-id="1dd04-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1dd04-129">PSContainerRegistry</span></span>
<span data-ttu-id="1dd04-130">' Registry ' 매개 변수는 파이프라인에서 ' PSContainerRegistry ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd04-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="1dd04-131">출력</span><span class="sxs-lookup"><span data-stu-id="1dd04-131">OUTPUTS</span></span>

### <span data-ttu-id="1dd04-132">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1dd04-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="1dd04-133">상속자</span><span class="sxs-lookup"><span data-stu-id="1dd04-133">NOTES</span></span>

## <span data-ttu-id="1dd04-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dd04-134">RELATED LINKS</span></span>

[<span data-ttu-id="1dd04-135">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1dd04-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="1dd04-136">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1dd04-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="1dd04-137">업데이트-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1dd04-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

