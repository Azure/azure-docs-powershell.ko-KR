---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fc8e454328706243e701c0f4df61733562ab73ce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876504"
---
# <span data-ttu-id="f13dc-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f13dc-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="f13dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f13dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f13dc-103">응용 프로그램과 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="f13dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f13dc-104">SYNTAX</span></span>

### <span data-ttu-id="f13dc-105">ApplicationObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f13dc-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f13dc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13dc-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13dc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13dc-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13dc-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13dc-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f13dc-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f13dc-109">DESCRIPTION</span></span>
<span data-ttu-id="f13dc-110">Get-AzADAppCredential cmdlet을 사용 하 여 응용 프로그램과 연결 된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="f13dc-111">이 명령은 응용 프로그램과 연결 된 자격 증명 속성 (자격 증명 값 제외)을 모두 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="f13dc-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f13dc-112">EXAMPLES</span></span>

### <span data-ttu-id="f13dc-113">예제 1-개체 id 별 응용 프로그램 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="f13dc-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="f13dc-114">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램과 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="f13dc-115">예제 2-파이핑을 기준으로 응용 프로그램 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="f13dc-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="f13dc-116">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램을 가져오고이를 Get-AzADAppCredential cmdlet에 파이프 하 여 해당 응용 프로그램의 모든 자격 증명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="f13dc-117">변수</span><span class="sxs-lookup"><span data-stu-id="f13dc-117">PARAMETERS</span></span>

### <span data-ttu-id="f13dc-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f13dc-118">-ApplicationId</span></span>
<span data-ttu-id="f13dc-119">자격 증명을 검색할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13dc-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="f13dc-120">-ApplicationObject</span></span>
<span data-ttu-id="f13dc-121">자격 증명을 검색할 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13dc-122">-DefaultProfile</span></span>
<span data-ttu-id="f13dc-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f13dc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f13dc-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f13dc-124">-DisplayName</span></span>
<span data-ttu-id="f13dc-125">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-125">The display name of the application.</span></span>

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

### <span data-ttu-id="f13dc-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f13dc-126">-ObjectId</span></span>
<span data-ttu-id="f13dc-127">자격 증명을 검색할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13dc-128">CommonParameters</span></span>
<span data-ttu-id="f13dc-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f13dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13dc-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f13dc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13dc-131">입력</span><span class="sxs-lookup"><span data-stu-id="f13dc-131">INPUTS</span></span>

### <span data-ttu-id="f13dc-132">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="f13dc-132">System.Guid</span></span>

### <span data-ttu-id="f13dc-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f13dc-133">System.String</span></span>

### <span data-ttu-id="f13dc-134">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="f13dc-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="f13dc-135">매개 변수: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f13dc-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="f13dc-136">출력</span><span class="sxs-lookup"><span data-stu-id="f13dc-136">OUTPUTS</span></span>

### <span data-ttu-id="f13dc-137">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="f13dc-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f13dc-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f13dc-138">NOTES</span></span>

## <span data-ttu-id="f13dc-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f13dc-139">RELATED LINKS</span></span>

[<span data-ttu-id="f13dc-140">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f13dc-140">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="f13dc-141">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f13dc-141">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="f13dc-142">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f13dc-142">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

