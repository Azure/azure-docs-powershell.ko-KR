---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 94a6b1ed2d02e3072a23ccc82fc4a49149b2ae2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876409"
---
# <span data-ttu-id="2dd40-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2dd40-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="2dd40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dd40-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd40-103">응용 프로그램에서 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="2dd40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dd40-104">SYNTAX</span></span>

### <span data-ttu-id="2dd40-105">ApplicationObjectIdWithKeyIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2dd40-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd40-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd40-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd40-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd40-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd40-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd40-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd40-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2dd40-109">DESCRIPTION</span></span>
<span data-ttu-id="2dd40-110">Remove-AzADAppCredential cmdlet은 손상 또는 자격 증명 키 롤오버 만료의 일부로 인해 응용 프로그램에서 자격 증명 키를 제거 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="2dd40-111">응용 프로그램은 개체 ID 또는 AppId를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="2dd40-112">제거할 자격 증명은 해당 키 ID로 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="2dd40-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2dd40-113">EXAMPLES</span></span>

### <span data-ttu-id="2dd40-114">예제 1-응용 프로그램에서 특정 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="2dd40-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="2dd40-115">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 응용 프로그램에서 키 id가 9044423a-60a3-45ac-9ab1-09534157ebb ' 인 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="2dd40-116">예제 2-응용 프로그램에서 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="2dd40-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="2dd40-117">응용 프로그램 id가 ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 ' 인 응용 프로그램에서 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="2dd40-118">예제 3-파이핑을 사용 하 여 모든 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="2dd40-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="2dd40-119">개체 id가 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' 인 응용 프로그램을 가져오고 Remove-AzADAppCredential cmdlet에 대 한 파이프를 사용 하 여 해당 응용 프로그램에서 모든 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="2dd40-120">변수</span><span class="sxs-lookup"><span data-stu-id="2dd40-120">PARAMETERS</span></span>

### <span data-ttu-id="2dd40-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2dd40-121">-ApplicationId</span></span>
<span data-ttu-id="2dd40-122">자격 증명을 제거할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="2dd40-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2dd40-123">-ApplicationObject</span></span>
<span data-ttu-id="2dd40-124">자격 증명을 제거할 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="2dd40-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd40-125">-DefaultProfile</span></span>
<span data-ttu-id="2dd40-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2dd40-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd40-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2dd40-127">-DisplayName</span></span>
<span data-ttu-id="2dd40-128">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-128">The display name of the application.</span></span>

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

### <span data-ttu-id="2dd40-129">-Force</span><span class="sxs-lookup"><span data-stu-id="2dd40-129">-Force</span></span>
<span data-ttu-id="2dd40-130">확인 하지 않고 자격 증명 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="2dd40-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2dd40-131">-KeyId</span></span>
<span data-ttu-id="2dd40-132">제거할 자격 증명 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="2dd40-133">응용 프로그램의 키 Id는 Get-AzADAppCredential cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="2dd40-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2dd40-134">-ObjectId</span></span>
<span data-ttu-id="2dd40-135">자격 증명을 제거할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="2dd40-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd40-136">-PassThru</span></span>
<span data-ttu-id="2dd40-137">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2dd40-138">-확인</span><span class="sxs-lookup"><span data-stu-id="2dd40-138">-Confirm</span></span>
<span data-ttu-id="2dd40-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd40-140">-WhatIf</span></span>
<span data-ttu-id="2dd40-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd40-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd40-143">CommonParameters</span></span>
<span data-ttu-id="2dd40-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dd40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd40-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dd40-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd40-146">입력</span><span class="sxs-lookup"><span data-stu-id="2dd40-146">INPUTS</span></span>

### <span data-ttu-id="2dd40-147">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="2dd40-147">System.Guid</span></span>

### <span data-ttu-id="2dd40-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2dd40-148">System.String</span></span>

### <span data-ttu-id="2dd40-149">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="2dd40-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="2dd40-150">매개 변수: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2dd40-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="2dd40-151">출력</span><span class="sxs-lookup"><span data-stu-id="2dd40-151">OUTPUTS</span></span>

### <span data-ttu-id="2dd40-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2dd40-152">System.Boolean</span></span>

## <span data-ttu-id="2dd40-153">상속자</span><span class="sxs-lookup"><span data-stu-id="2dd40-153">NOTES</span></span>

## <span data-ttu-id="2dd40-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dd40-154">RELATED LINKS</span></span>

[<span data-ttu-id="2dd40-155">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2dd40-155">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="2dd40-156">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2dd40-156">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="2dd40-157">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2dd40-157">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
