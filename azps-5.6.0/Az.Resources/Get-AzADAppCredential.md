---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: c96fceb331a2b33528b47506e928ea78cfc793d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974475"
---
# <span data-ttu-id="590b0-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="590b0-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="590b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="590b0-102">SYNOPSIS</span></span>
<span data-ttu-id="590b0-103">애플리케이션과 연결된 자격 증명 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="590b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="590b0-104">SYNTAX</span></span>

### <span data-ttu-id="590b0-105">ApplicationObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="590b0-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590b0-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="590b0-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590b0-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="590b0-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="590b0-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="590b0-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="590b0-109">설명</span><span class="sxs-lookup"><span data-stu-id="590b0-109">DESCRIPTION</span></span>
<span data-ttu-id="590b0-110">Get-AzADAppCredential cmdlet을 사용하여 애플리케이션과 연결된 자격 증명 목록을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="590b0-111">이 명령은 애플리케이션과 연결된 모든 자격 증명 속성(자격 증명 값은 검색하지 않지만)을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="590b0-112">예제</span><span class="sxs-lookup"><span data-stu-id="590b0-112">EXAMPLES</span></span>

### <span data-ttu-id="590b0-113">예제 1: 개체 ID로 애플리케이션 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="590b0-114">개체 ID '1f99cf81-0146-4f4e-beae-2007d0668476'을 갖는 애플리케이션과 관련된 자격 증명 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="590b0-115">예제 2: 파이핑을 통해 애플리케이션 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="590b0-116">개체 ID '1f99cf81-0146-4f4e-beae-2007d0668476'을 사용하여 애플리케이션을 Get-AzADAppCredential cmdlet에 파이프하여 해당 애플리케이션에 대한 모든 자격 증명을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="590b0-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="590b0-117">PARAMETERS</span></span>

### <span data-ttu-id="590b0-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="590b0-118">-ApplicationId</span></span>
<span data-ttu-id="590b0-119">자격 증명을 검색하는 애플리케이션의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="590b0-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="590b0-120">-ApplicationObject</span></span>
<span data-ttu-id="590b0-121">에서 자격 증명을 검색하는 애플리케이션 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="590b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590b0-122">-DefaultProfile</span></span>
<span data-ttu-id="590b0-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="590b0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="590b0-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="590b0-124">-DisplayName</span></span>
<span data-ttu-id="590b0-125">애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-125">The display name of the application.</span></span>

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

### <span data-ttu-id="590b0-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="590b0-126">-ObjectId</span></span>
<span data-ttu-id="590b0-127">자격 증명을 검색하는 애플리케이션의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="590b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590b0-128">CommonParameters</span></span>
<span data-ttu-id="590b0-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="590b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590b0-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="590b0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590b0-131">입력</span><span class="sxs-lookup"><span data-stu-id="590b0-131">INPUTS</span></span>

### <span data-ttu-id="590b0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="590b0-132">System.String</span></span>

### <span data-ttu-id="590b0-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="590b0-133">System.Guid</span></span>

### <span data-ttu-id="590b0-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="590b0-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="590b0-135">출력</span><span class="sxs-lookup"><span data-stu-id="590b0-135">OUTPUTS</span></span>

### <span data-ttu-id="590b0-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="590b0-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="590b0-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="590b0-137">NOTES</span></span>

## <span data-ttu-id="590b0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="590b0-138">RELATED LINKS</span></span>

[<span data-ttu-id="590b0-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="590b0-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="590b0-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="590b0-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="590b0-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="590b0-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

