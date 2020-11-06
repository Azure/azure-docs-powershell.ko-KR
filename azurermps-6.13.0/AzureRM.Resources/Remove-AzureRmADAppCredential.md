---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528409"
---
# <span data-ttu-id="c9494-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c9494-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="c9494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9494-102">SYNOPSIS</span></span>
<span data-ttu-id="c9494-103">응용 프로그램에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9494-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9494-104">SYNTAX</span></span>

### <span data-ttu-id="c9494-105">ApplicationObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9494-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9494-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9494-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9494-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9494-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9494-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9494-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9494-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c9494-109">DESCRIPTION</span></span>
<span data-ttu-id="c9494-110">Remove-AzureRmADAppCredential cmdlet은 손상 또는 자격 증명 키 롤오버 만료의 일부로 인해 응용 프로그램에서 자격 증명 키를 제거 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c9494-111">응용 프로그램은 개체 ID 또는 AppId를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="c9494-112">제거할 자격 증명은 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="c9494-113">예제의</span><span class="sxs-lookup"><span data-stu-id="c9494-113">EXAMPLES</span></span>

### <span data-ttu-id="c9494-114">예제 1-응용 프로그램에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="c9494-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c9494-115">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 응용 프로그램에서 키 id가 9044423a-60a3-45ac-9ab1-09534157ebb ' 인 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="c9494-116">예제 2-응용 프로그램에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="c9494-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="c9494-117">응용 프로그램 id가 ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 ' 인 응용 프로그램에서 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="c9494-118">예제 3-파이핑을 사용 하 여 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="c9494-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="c9494-119">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 응용 프로그램을 가져오고 Remove-AzureRmADAppCredential cmdlet에 대 한 파이프를 사용 하 여 해당 응용 프로그램에서 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="c9494-120">변수</span><span class="sxs-lookup"><span data-stu-id="c9494-120">PARAMETERS</span></span>

### <span data-ttu-id="c9494-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9494-121">-ApplicationId</span></span>
<span data-ttu-id="c9494-122">자격 증명을 제거할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9494-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c9494-123">-ApplicationObject</span></span>
<span data-ttu-id="c9494-124">자격 증명을 제거할 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9494-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9494-125">-DefaultProfile</span></span>
<span data-ttu-id="c9494-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9494-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9494-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c9494-127">-DisplayName</span></span>
<span data-ttu-id="c9494-128">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9494-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c9494-129">-Force</span></span>
<span data-ttu-id="c9494-130">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="c9494-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c9494-131">-KeyId</span></span>
<span data-ttu-id="c9494-132">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c9494-133">응용 프로그램의 키 Id는 Get-AzureRmADAppCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9494-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9494-134">-ObjectId</span></span>
<span data-ttu-id="c9494-135">자격 증명을 제거할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9494-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9494-136">-PassThru</span></span>
<span data-ttu-id="c9494-137">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c9494-138">-확인</span><span class="sxs-lookup"><span data-stu-id="c9494-138">-Confirm</span></span>
<span data-ttu-id="c9494-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9494-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9494-140">-WhatIf</span></span>
<span data-ttu-id="c9494-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9494-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9494-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9494-143">CommonParameters</span></span>
<span data-ttu-id="c9494-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9494-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9494-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9494-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9494-146">입력</span><span class="sxs-lookup"><span data-stu-id="c9494-146">INPUTS</span></span>

### <span data-ttu-id="c9494-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c9494-147">System.Guid</span></span>

### <span data-ttu-id="c9494-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c9494-148">System.String</span></span>

### <span data-ttu-id="c9494-149">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="c9494-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="c9494-150">매개 변수: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9494-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="c9494-151">출력</span><span class="sxs-lookup"><span data-stu-id="c9494-151">OUTPUTS</span></span>

### <span data-ttu-id="c9494-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c9494-152">System.Boolean</span></span>

## <span data-ttu-id="c9494-153">상속자</span><span class="sxs-lookup"><span data-stu-id="c9494-153">NOTES</span></span>

## <span data-ttu-id="c9494-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9494-154">RELATED LINKS</span></span>

[<span data-ttu-id="c9494-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c9494-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c9494-156">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c9494-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="c9494-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c9494-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
