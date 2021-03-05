---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961696"
---
# <span data-ttu-id="8a14c-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a14c-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="8a14c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a14c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a14c-103">서비스 주체와 연결된 자격 증명 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="8a14c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a14c-104">SYNTAX</span></span>

### <span data-ttu-id="8a14c-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8a14c-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a14c-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a14c-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a14c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a14c-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a14c-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a14c-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a14c-109">설명</span><span class="sxs-lookup"><span data-stu-id="8a14c-109">DESCRIPTION</span></span>
<span data-ttu-id="8a14c-110">Get-AzADSpCredential cmdlet을 사용하여 서비스 주체와 연결된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="8a14c-111">이 명령은 서비스 주체와 연결된 모든 자격 증명 속성(자격 증명 값은 검색하지 않지만)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="8a14c-112">예제</span><span class="sxs-lookup"><span data-stu-id="8a14c-112">EXAMPLES</span></span>

### <span data-ttu-id="8a14c-113">예제 1 - SPN에 의해 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="8a14c-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="8a14c-114">SPN '을 사용하여 서비스 주체와 연결된 자격 증명 목록을 http://test12345 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="8a14c-115">예제 2 - 개체 ID에 따라 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="8a14c-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="8a14c-116">개체 ID "58e28616-99cc-4da4-b705-7672130e1047"을 사용하여 서비스 주체와 연결된 자격 증명 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="8a14c-117">예제 3 - 파이핑으로 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="8a14c-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="8a14c-118">개체 ID "58e28616-99cc-4da4-b705-7672130e1047"을 사용하여 서비스 주체에 대한 모든 자격 증명을 Get-AzADSpCredential cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="8a14c-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a14c-119">PARAMETERS</span></span>

### <span data-ttu-id="8a14c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a14c-120">-DefaultProfile</span></span>
<span data-ttu-id="8a14c-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8a14c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a14c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a14c-122">-DisplayName</span></span>
<span data-ttu-id="8a14c-123">서비스 주체의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="8a14c-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a14c-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8a14c-124">-ObjectId</span></span>
<span data-ttu-id="8a14c-125">자격 증명을 검색하는 서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a14c-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8a14c-126">-ServicePrincipalName</span></span>
<span data-ttu-id="8a14c-127">자격 증명을 검색하는 서비스 주체의 SPN(이름)입니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a14c-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="8a14c-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="8a14c-129">자격 증명을 검색하는 서비스 주체 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a14c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a14c-130">CommonParameters</span></span>
<span data-ttu-id="8a14c-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a14c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a14c-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a14c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a14c-133">입력</span><span class="sxs-lookup"><span data-stu-id="8a14c-133">INPUTS</span></span>

### <span data-ttu-id="8a14c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8a14c-134">System.String</span></span>

### <span data-ttu-id="8a14c-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8a14c-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="8a14c-136">출력</span><span class="sxs-lookup"><span data-stu-id="8a14c-136">OUTPUTS</span></span>

### <span data-ttu-id="8a14c-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="8a14c-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="8a14c-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a14c-138">NOTES</span></span>

## <span data-ttu-id="8a14c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a14c-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a14c-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a14c-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="8a14c-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8a14c-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="8a14c-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8a14c-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

