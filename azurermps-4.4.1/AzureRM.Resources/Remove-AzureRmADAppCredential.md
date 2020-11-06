---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532952"
---
# <span data-ttu-id="d55f8-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d55f8-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="d55f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d55f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d55f8-103">응용 프로그램에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d55f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d55f8-104">SYNTAX</span></span>

### <span data-ttu-id="d55f8-105">ApplicationObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d55f8-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55f8-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="d55f8-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55f8-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d55f8-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55f8-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="d55f8-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55f8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d55f8-109">DESCRIPTION</span></span>
<span data-ttu-id="d55f8-110">Remove-AzureRmADAppCredential cmdlet은 손상 또는 자격 증명 키 롤오버 만료의 일부로 인해 응용 프로그램에서 자격 증명 키를 제거 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="d55f8-111">응용 프로그램은 개체 ID 또는 AppId를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="d55f8-112">제거할 자격 증명은 개별 자격 증명을 제거 하거나 ' 모두 ' 스위치를 사용 하 여 응용 프로그램과 연결 된 모든 자격 증명을 삭제 하는 경우 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="d55f8-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d55f8-113">EXAMPLES</span></span>

### <span data-ttu-id="d55f8-114">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d55f8-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="d55f8-115">이 명령은 응용 프로그램에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="d55f8-116">이 예제에서는 Id "9044423a-60a3-45ac-9ab1-09534157ebb"가 있는 키가 응용 프로그램에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="d55f8-117">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d55f8-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="d55f8-118">이 명령은 응용 프로그램에서 자격 증명 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="d55f8-119">이 예제에서는 모든 자격 증명이 applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58"와 연결 된 응용 프로그램에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="d55f8-120">변수</span><span class="sxs-lookup"><span data-stu-id="d55f8-120">PARAMETERS</span></span>

### <span data-ttu-id="d55f8-121">-All</span><span class="sxs-lookup"><span data-stu-id="d55f8-121">-All</span></span>
<span data-ttu-id="d55f8-122">스위치를 사용 하 여 응용 프로그램과 연결 된 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55f8-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d55f8-123">-ApplicationId</span></span>
<span data-ttu-id="d55f8-124">자격 증명을 제거할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55f8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d55f8-125">-Force</span></span>
<span data-ttu-id="d55f8-126">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55f8-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d55f8-127">-KeyId</span></span>
<span data-ttu-id="d55f8-128">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="d55f8-129">응용 프로그램의 키 Id는 Get-AzureRmADAppCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55f8-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d55f8-130">-ObjectId</span></span>
<span data-ttu-id="d55f8-131">자격 증명을 제거할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55f8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d55f8-132">-Confirm</span></span>
<span data-ttu-id="d55f8-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55f8-134">-WhatIf</span></span>
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

### <span data-ttu-id="d55f8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55f8-135">-DefaultProfile</span></span>
<span data-ttu-id="d55f8-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d55f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55f8-137">CommonParameters</span></span>
<span data-ttu-id="d55f8-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d55f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55f8-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55f8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55f8-140">입력</span><span class="sxs-lookup"><span data-stu-id="d55f8-140">INPUTS</span></span>

## <span data-ttu-id="d55f8-141">출력</span><span class="sxs-lookup"><span data-stu-id="d55f8-141">OUTPUTS</span></span>

## <span data-ttu-id="d55f8-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d55f8-142">NOTES</span></span>

## <span data-ttu-id="d55f8-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d55f8-143">RELATED LINKS</span></span>

[<span data-ttu-id="d55f8-144">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d55f8-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="d55f8-145">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d55f8-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="d55f8-146">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d55f8-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
