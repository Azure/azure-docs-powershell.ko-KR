---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703222"
---
# <span data-ttu-id="e0b18-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0b18-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="e0b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0b18-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b18-103">Azure active directory 서비스 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0b18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0b18-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0b18-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b18-106">Azure active directory 서비스 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="e0b18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e0b18-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b18-108">AAD 서비스 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="e0b18-109">지정 된 azure active directory 서비스 주체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="e0b18-110">변수</span><span class="sxs-lookup"><span data-stu-id="e0b18-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b18-111">-DefaultProfile</span></span>
<span data-ttu-id="e0b18-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e0b18-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0b18-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e0b18-113">-Force</span></span>
<span data-ttu-id="e0b18-114">{{Force 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="e0b18-114">{{Fill Force Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b18-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e0b18-115">-ObjectId</span></span>
<span data-ttu-id="e0b18-116">삭제할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b18-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b18-117">-PassThru</span></span>
<span data-ttu-id="e0b18-118">지정 된 경우 삭제 된 서비스 사용자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-118">If specified, returns the deleted service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b18-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e0b18-119">-Confirm</span></span>
<span data-ttu-id="e0b18-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b18-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b18-121">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b18-122">CommonParameters</span></span>
<span data-ttu-id="e0b18-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b18-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b18-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b18-125">입력</span><span class="sxs-lookup"><span data-stu-id="e0b18-125">INPUTS</span></span>

### <span data-ttu-id="e0b18-126">않아야</span><span class="sxs-lookup"><span data-stu-id="e0b18-126">None</span></span>
<span data-ttu-id="e0b18-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0b18-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0b18-128">출력</span><span class="sxs-lookup"><span data-stu-id="e0b18-128">OUTPUTS</span></span>

### <span data-ttu-id="e0b18-129">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal</span><span class="sxs-lookup"><span data-stu-id="e0b18-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e0b18-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e0b18-130">NOTES</span></span>
<span data-ttu-id="e0b18-131">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="e0b18-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e0b18-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0b18-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0b18-133">새로운 AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0b18-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0b18-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0b18-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0b18-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0b18-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0b18-136">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e0b18-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="e0b18-137">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e0b18-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
