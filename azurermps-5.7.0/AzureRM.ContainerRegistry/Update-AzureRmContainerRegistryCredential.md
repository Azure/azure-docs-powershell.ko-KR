---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531080"
---
# <span data-ttu-id="41586-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="41586-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="41586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41586-102">SYNOPSIS</span></span>
<span data-ttu-id="41586-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41586-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41586-104">SYNTAX</span></span>

### <span data-ttu-id="41586-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="41586-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41586-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41586-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41586-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41586-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41586-108">설명은</span><span class="sxs-lookup"><span data-stu-id="41586-108">DESCRIPTION</span></span>
<span data-ttu-id="41586-109">Update-AzureRmContainerRegistryCredential cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="41586-110">예제의</span><span class="sxs-lookup"><span data-stu-id="41586-110">EXAMPLES</span></span>

### <span data-ttu-id="41586-111">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 다시 생성</span><span class="sxs-lookup"><span data-stu-id="41586-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="41586-112">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="41586-113">\` \` 로그인 자격 증명을 다시 생성 하기 위해 관리 사용자에 게 컨테이너 레지스트리 myregistry을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="41586-114">변수</span><span class="sxs-lookup"><span data-stu-id="41586-114">PARAMETERS</span></span>

### <span data-ttu-id="41586-115">-이름</span><span class="sxs-lookup"><span data-stu-id="41586-115">-Name</span></span>
<span data-ttu-id="41586-116">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41586-116">Container Registry Name.</span></span>

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

### <span data-ttu-id="41586-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="41586-117">-PasswordName</span></span>
<span data-ttu-id="41586-118">다시 생성할 암호의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41586-118">The name of password to regenerate.</span></span>
<span data-ttu-id="41586-119">허용 되는 값: password, password2.</span><span class="sxs-lookup"><span data-stu-id="41586-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41586-120">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="41586-120">-Registry</span></span>
<span data-ttu-id="41586-121">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="41586-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41586-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41586-122">-ResourceGroupName</span></span>
<span data-ttu-id="41586-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41586-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="41586-124">-확인</span><span class="sxs-lookup"><span data-stu-id="41586-124">-Confirm</span></span>
<span data-ttu-id="41586-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41586-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41586-126">-WhatIf</span></span>
<span data-ttu-id="41586-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="41586-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41586-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41586-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41586-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41586-129">-DefaultProfile</span></span>
<span data-ttu-id="41586-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="41586-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41586-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41586-131">-ResourceId</span></span>
<span data-ttu-id="41586-132">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="41586-132">The container registry resource id</span></span>

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

### <span data-ttu-id="41586-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41586-133">CommonParameters</span></span>
<span data-ttu-id="41586-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41586-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41586-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41586-136">입력</span><span class="sxs-lookup"><span data-stu-id="41586-136">INPUTS</span></span>

### <span data-ttu-id="41586-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41586-137">PSContainerRegistry</span></span>
<span data-ttu-id="41586-138">' Registry ' 매개 변수는 파이프라인에서 ' PSContainerRegistry ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="41586-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="41586-139">출력</span><span class="sxs-lookup"><span data-stu-id="41586-139">OUTPUTS</span></span>

### <span data-ttu-id="41586-140">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="41586-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="41586-141">상속자</span><span class="sxs-lookup"><span data-stu-id="41586-141">NOTES</span></span>

## <span data-ttu-id="41586-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41586-142">RELATED LINKS</span></span>

[<span data-ttu-id="41586-143">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41586-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="41586-144">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41586-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="41586-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="41586-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

