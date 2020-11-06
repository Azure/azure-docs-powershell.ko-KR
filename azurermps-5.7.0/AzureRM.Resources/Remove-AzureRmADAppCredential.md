---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526612"
---
# <span data-ttu-id="089ca-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="089ca-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="089ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089ca-102">SYNOPSIS</span></span>
<span data-ttu-id="089ca-103">응용 프로그램에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="089ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="089ca-104">SYNTAX</span></span>

### <span data-ttu-id="089ca-105">ApplicationObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="089ca-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="089ca-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="089ca-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="089ca-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="089ca-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="089ca-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="089ca-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="089ca-109">설명은</span><span class="sxs-lookup"><span data-stu-id="089ca-109">DESCRIPTION</span></span>
<span data-ttu-id="089ca-110">Remove-AzureRmADAppCredential cmdlet은 손상 또는 자격 증명 키 롤오버 만료의 일부로 인해 응용 프로그램에서 자격 증명 키를 제거 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="089ca-111">응용 프로그램은 개체 ID 또는 AppId를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="089ca-112">제거할 자격 증명은 개별 자격 증명을 제거 하거나 ' 모두 ' 스위치를 사용 하 여 응용 프로그램과 연결 된 모든 자격 증명을 삭제 하는 경우 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="089ca-113">예제의</span><span class="sxs-lookup"><span data-stu-id="089ca-113">EXAMPLES</span></span>

### <span data-ttu-id="089ca-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="089ca-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="089ca-115">이 명령은 응용 프로그램에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="089ca-116">이 예제에서는 Id "9044423a-60a3-45ac-9ab1-09534157ebb"가 있는 키가 응용 프로그램에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="089ca-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="089ca-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="089ca-118">이 명령은 응용 프로그램에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="089ca-119">이 예제에서는 모든 자격 증명이 applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58"와 연결 된 응용 프로그램에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="089ca-120">변수</span><span class="sxs-lookup"><span data-stu-id="089ca-120">PARAMETERS</span></span>

### <span data-ttu-id="089ca-121">-All</span><span class="sxs-lookup"><span data-stu-id="089ca-121">-All</span></span>
<span data-ttu-id="089ca-122">스위치를 사용 하 여 응용 프로그램과 연결 된 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="089ca-123">-ApplicationId</span></span>
<span data-ttu-id="089ca-124">자격 증명을 제거할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089ca-125">-DefaultProfile</span></span>
<span data-ttu-id="089ca-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="089ca-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="089ca-127">-Force</span><span class="sxs-lookup"><span data-stu-id="089ca-127">-Force</span></span>
<span data-ttu-id="089ca-128">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-128">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="089ca-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="089ca-129">-KeyId</span></span>
<span data-ttu-id="089ca-130">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="089ca-131">응용 프로그램의 키 Id는 Get-AzureRmADAppCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="089ca-132">-ObjectId</span></span>
<span data-ttu-id="089ca-133">자격 증명을 제거할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-134">-확인</span><span class="sxs-lookup"><span data-stu-id="089ca-134">-Confirm</span></span>
<span data-ttu-id="089ca-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="089ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="089ca-136">-WhatIf</span></span>
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

### <span data-ttu-id="089ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089ca-137">CommonParameters</span></span>
<span data-ttu-id="089ca-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089ca-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089ca-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089ca-140">입력</span><span class="sxs-lookup"><span data-stu-id="089ca-140">INPUTS</span></span>

### <span data-ttu-id="089ca-141">않아야</span><span class="sxs-lookup"><span data-stu-id="089ca-141">None</span></span>
<span data-ttu-id="089ca-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="089ca-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="089ca-143">출력</span><span class="sxs-lookup"><span data-stu-id="089ca-143">OUTPUTS</span></span>

## <span data-ttu-id="089ca-144">상속자</span><span class="sxs-lookup"><span data-stu-id="089ca-144">NOTES</span></span>

## <span data-ttu-id="089ca-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="089ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="089ca-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="089ca-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="089ca-147">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="089ca-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="089ca-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="089ca-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)