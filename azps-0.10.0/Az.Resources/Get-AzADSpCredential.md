---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 40543468145c7fcfaf49fcfc7cad1cbf70938adf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876498"
---
# <span data-ttu-id="c76cf-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c76cf-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="c76cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c76cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c76cf-103">서비스 사용자와 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="c76cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c76cf-104">SYNTAX</span></span>

### <span data-ttu-id="c76cf-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c76cf-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c76cf-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76cf-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c76cf-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76cf-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c76cf-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c76cf-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c76cf-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c76cf-109">DESCRIPTION</span></span>
<span data-ttu-id="c76cf-110">Get-AzADSpCredential cmdlet은 서비스 사용자와 연결 된 자격 증명 목록을 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="c76cf-111">이 명령은 서비스 사용자와 연결 된 모든 자격 증명 속성 (자격 증명 값 제외)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="c76cf-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c76cf-112">EXAMPLES</span></span>

### <span data-ttu-id="c76cf-113">예제 1-SPN으로 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="c76cf-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="c76cf-114">SPN이 있는 서비스 사용자와 연결 된 자격 증명 목록을 반환 http://test12345 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="c76cf-115">예제 2-개체 id 별 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="c76cf-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="c76cf-116">개체 id가 "58e28616-99cc-4da4-b705-7672130e1047" 인 서비스 사용자와 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="c76cf-117">예제 3-파이핑으로 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="c76cf-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="c76cf-118">개체 id가 "58e28616-99cc-4da4-b705-7672130e1047" 인 서비스 사용자를 가져오고이를 Get-AzADSpCredential cmdlet에 파이프 하 여 해당 서비스 사용자의 모든 자격 증명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="c76cf-119">변수</span><span class="sxs-lookup"><span data-stu-id="c76cf-119">PARAMETERS</span></span>

### <span data-ttu-id="c76cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76cf-120">-DefaultProfile</span></span>
<span data-ttu-id="c76cf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c76cf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c76cf-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c76cf-122">-DisplayName</span></span>
<span data-ttu-id="c76cf-123">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="c76cf-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c76cf-124">-ObjectId</span></span>
<span data-ttu-id="c76cf-125">자격 증명을 검색할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76cf-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c76cf-126">-ServicePrincipalName</span></span>
<span data-ttu-id="c76cf-127">자격 증명을 검색할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="c76cf-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="c76cf-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="c76cf-129">자격 증명을 검색할 서비스 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c76cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76cf-130">CommonParameters</span></span>
<span data-ttu-id="c76cf-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c76cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76cf-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76cf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76cf-133">입력</span><span class="sxs-lookup"><span data-stu-id="c76cf-133">INPUTS</span></span>

### <span data-ttu-id="c76cf-134">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c76cf-134">System.Guid</span></span>

### <span data-ttu-id="c76cf-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c76cf-135">System.String</span></span>

### <span data-ttu-id="c76cf-136">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal</span><span class="sxs-lookup"><span data-stu-id="c76cf-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="c76cf-137">매개 변수: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c76cf-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="c76cf-138">출력</span><span class="sxs-lookup"><span data-stu-id="c76cf-138">OUTPUTS</span></span>

### <span data-ttu-id="c76cf-139">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="c76cf-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c76cf-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c76cf-140">NOTES</span></span>

## <span data-ttu-id="c76cf-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c76cf-141">RELATED LINKS</span></span>

[<span data-ttu-id="c76cf-142">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c76cf-142">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="c76cf-143">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c76cf-143">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="c76cf-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c76cf-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

