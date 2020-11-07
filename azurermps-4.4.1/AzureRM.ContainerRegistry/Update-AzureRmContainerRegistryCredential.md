---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702707"
---
# <span data-ttu-id="fb2ec-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb2ec-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="fb2ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2ec-103">컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb2ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb2ec-104">SYNTAX</span></span>

### <span data-ttu-id="fb2ec-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb2ec-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb2ec-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb2ec-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb2ec-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb2ec-107">DESCRIPTION</span></span>
<span data-ttu-id="fb2ec-108">**업데이트 AzureRmContainerRegistryCredential** cmdlet은 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="fb2ec-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb2ec-109">EXAMPLES</span></span>

### <span data-ttu-id="fb2ec-110">예제 1: 컨테이너 레지스트리에 대 한 로그인 자격 증명 다시 생성</span><span class="sxs-lookup"><span data-stu-id="fb2ec-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="fb2ec-111">이 명령은 지정 된 컨테이너 레지스트리에 대 한 로그인 자격 증명을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="fb2ec-112">`MyRegistry`로그인 자격 증명을 다시 생성 하려면 관리자 사용자가 컨테이너 레지스트리에 대해 설정 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="fb2ec-113">변수</span><span class="sxs-lookup"><span data-stu-id="fb2ec-113">PARAMETERS</span></span>

### <span data-ttu-id="fb2ec-114">-이름</span><span class="sxs-lookup"><span data-stu-id="fb2ec-114">-Name</span></span>
<span data-ttu-id="fb2ec-115">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb2ec-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="fb2ec-116">-PasswordName</span></span>
<span data-ttu-id="fb2ec-117">다시 생성할 암호의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-117">The name of password to regenerate.</span></span>
<span data-ttu-id="fb2ec-118">허용 되는 값: password, password2.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb2ec-119">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="fb2ec-119">-Registry</span></span>
<span data-ttu-id="fb2ec-120">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="fb2ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb2ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb2ec-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb2ec-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fb2ec-123">-Confirm</span></span>
<span data-ttu-id="fb2ec-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2ec-125">-WhatIf</span></span>
<span data-ttu-id="fb2ec-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2ec-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2ec-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2ec-128">-DefaultProfile</span></span>
<span data-ttu-id="fb2ec-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb2ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2ec-130">CommonParameters</span></span>
<span data-ttu-id="fb2ec-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2ec-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2ec-133">입력</span><span class="sxs-lookup"><span data-stu-id="fb2ec-133">INPUTS</span></span>

### <span data-ttu-id="fb2ec-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb2ec-134">PSContainerRegistry</span></span>
<span data-ttu-id="fb2ec-135">' Registry ' 매개 변수는 파이프라인에서 ' PSContainerRegistry ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb2ec-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="fb2ec-136">출력</span><span class="sxs-lookup"><span data-stu-id="fb2ec-136">OUTPUTS</span></span>

### <span data-ttu-id="fb2ec-137">ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb2ec-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="fb2ec-138">상속자</span><span class="sxs-lookup"><span data-stu-id="fb2ec-138">NOTES</span></span>

## <span data-ttu-id="fb2ec-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb2ec-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb2ec-140">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb2ec-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fb2ec-141">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fb2ec-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="fb2ec-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="fb2ec-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

