---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212175"
---
# <span data-ttu-id="698ab-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="698ab-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="698ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="698ab-102">SYNOPSIS</span></span>
<span data-ttu-id="698ab-103">응용 프로그램과 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="698ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="698ab-104">SYNTAX</span></span>

### <span data-ttu-id="698ab-105">ApplicationObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="698ab-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="698ab-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="698ab-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="698ab-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="698ab-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="698ab-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="698ab-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="698ab-109">설명은</span><span class="sxs-lookup"><span data-stu-id="698ab-109">DESCRIPTION</span></span>
<span data-ttu-id="698ab-110">Get-AzADAppCredential cmdlet을 사용 하 여 응용 프로그램과 연결 된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="698ab-111">이 명령은 응용 프로그램과 연결 된 자격 증명 속성 (자격 증명 값 제외)을 모두 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="698ab-112">예제의</span><span class="sxs-lookup"><span data-stu-id="698ab-112">EXAMPLES</span></span>

### <span data-ttu-id="698ab-113">예제 1: 개체 id를 기준으로 응용 프로그램 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="698ab-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="698ab-114">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램과 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="698ab-115">예제 2: 파이핑을 기준으로 응용 프로그램 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="698ab-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="698ab-116">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 응용 프로그램을 가져오고이를 Get-AzADAppCredential cmdlet에 파이프 하 여 해당 응용 프로그램의 모든 자격 증명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="698ab-117">변수</span><span class="sxs-lookup"><span data-stu-id="698ab-117">PARAMETERS</span></span>

### <span data-ttu-id="698ab-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="698ab-118">-ApplicationId</span></span>
<span data-ttu-id="698ab-119">자격 증명을 검색할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="698ab-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="698ab-120">-ApplicationObject</span></span>
<span data-ttu-id="698ab-121">자격 증명을 검색할 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="698ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698ab-122">-DefaultProfile</span></span>
<span data-ttu-id="698ab-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="698ab-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="698ab-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="698ab-124">-DisplayName</span></span>
<span data-ttu-id="698ab-125">응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-125">The display name of the application.</span></span>

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

### <span data-ttu-id="698ab-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="698ab-126">-ObjectId</span></span>
<span data-ttu-id="698ab-127">자격 증명을 검색할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="698ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698ab-128">CommonParameters</span></span>
<span data-ttu-id="698ab-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="698ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698ab-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="698ab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698ab-131">입력</span><span class="sxs-lookup"><span data-stu-id="698ab-131">INPUTS</span></span>

### <span data-ttu-id="698ab-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="698ab-132">System.String</span></span>

### <span data-ttu-id="698ab-133">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="698ab-133">System.Guid</span></span>

### <span data-ttu-id="698ab-134">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="698ab-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="698ab-135">출력</span><span class="sxs-lookup"><span data-stu-id="698ab-135">OUTPUTS</span></span>

### <span data-ttu-id="698ab-136">ActiveDirectory Adcredential 자격 증명</span><span class="sxs-lookup"><span data-stu-id="698ab-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="698ab-137">상속자</span><span class="sxs-lookup"><span data-stu-id="698ab-137">NOTES</span></span>

## <span data-ttu-id="698ab-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="698ab-138">RELATED LINKS</span></span>

[<span data-ttu-id="698ab-139">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="698ab-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="698ab-140">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="698ab-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="698ab-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="698ab-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

