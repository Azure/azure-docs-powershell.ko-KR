---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534716"
---
# <span data-ttu-id="896e5-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="896e5-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="896e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896e5-102">SYNOPSIS</span></span>
<span data-ttu-id="896e5-103">서비스 사용자에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="896e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="896e5-104">SYNTAX</span></span>

### <span data-ttu-id="896e5-105">ObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="896e5-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896e5-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="896e5-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896e5-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="896e5-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896e5-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="896e5-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="896e5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="896e5-109">DESCRIPTION</span></span>
<span data-ttu-id="896e5-110">Remove-AzureRmADSpCredential cmdlet을 사용 하 여 손상 되거나 자격 증명 키 롤오버 만료의 일부인 경우 서비스 사용자가 자격 증명 키를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="896e5-111">서비스 사용자는 개체 ID 또는 SPN (서비스 사용자 이름) 중 하나를 제공 하 여 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="896e5-112">제거할 자격 증명은 개별 자격 증명을 제거 하거나 ' 모두 ' 스위치를 사용 하 여 서비스 사용자와 연결 된 모든 자격 증명을 삭제 하는 경우 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="896e5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="896e5-113">EXAMPLES</span></span>

### <span data-ttu-id="896e5-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="896e5-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="896e5-115">이 명령은 서비스 사용자에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="896e5-116">이 예제에서는 Id "9044423a-60a3-45ac-9ab1-09534157ebb" 키가 서비스 사용자에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="896e5-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="896e5-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="896e5-118">이 명령은 서비스 사용자에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="896e5-119">이 예제에서는 모든 자격 증명이 서비스 사용자 이름 ""과 관련 된 서비스 사용자에서 제거 됩니다 http://test123 .</span><span class="sxs-lookup"><span data-stu-id="896e5-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="896e5-120">변수</span><span class="sxs-lookup"><span data-stu-id="896e5-120">PARAMETERS</span></span>

### <span data-ttu-id="896e5-121">-All</span><span class="sxs-lookup"><span data-stu-id="896e5-121">-All</span></span>
<span data-ttu-id="896e5-122">스위치를 사용 하 여 서비스 사용자와 연결 된 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896e5-123">-DefaultProfile</span></span>
<span data-ttu-id="896e5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="896e5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="896e5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="896e5-125">-Force</span></span>
<span data-ttu-id="896e5-126">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="896e5-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="896e5-127">-KeyId</span></span>
<span data-ttu-id="896e5-128">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="896e5-129">서비스 사용자의 키 Id는 Get-AzureRmADSpCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896e5-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="896e5-130">-ObjectId</span></span>
<span data-ttu-id="896e5-131">자격 증명을 제거할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896e5-132">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="896e5-132">-ServicePrincipalName</span></span>
<span data-ttu-id="896e5-133">자격 증명을 제거할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896e5-134">-확인</span><span class="sxs-lookup"><span data-stu-id="896e5-134">-Confirm</span></span>
<span data-ttu-id="896e5-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="896e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="896e5-136">-WhatIf</span></span>
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

### <span data-ttu-id="896e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896e5-137">CommonParameters</span></span>
<span data-ttu-id="896e5-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896e5-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="896e5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896e5-140">입력</span><span class="sxs-lookup"><span data-stu-id="896e5-140">INPUTS</span></span>

### <span data-ttu-id="896e5-141">않아야</span><span class="sxs-lookup"><span data-stu-id="896e5-141">None</span></span>
<span data-ttu-id="896e5-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="896e5-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="896e5-143">출력</span><span class="sxs-lookup"><span data-stu-id="896e5-143">OUTPUTS</span></span>

## <span data-ttu-id="896e5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="896e5-144">NOTES</span></span>

## <span data-ttu-id="896e5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="896e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="896e5-146">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="896e5-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="896e5-147">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="896e5-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="896e5-148">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="896e5-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

