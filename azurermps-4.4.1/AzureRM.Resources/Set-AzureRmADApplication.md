---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711497"
---
# <span data-ttu-id="0f5a6-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f5a6-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="0f5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5a6-103">기존 azure active directory 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f5a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f5a6-104">SYNTAX</span></span>

### <span data-ttu-id="0f5a6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f5a6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f5a6-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f5a6-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f5a6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f5a6-107">DESCRIPTION</span></span>
<span data-ttu-id="0f5a6-108">기존 azure active directory 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="0f5a6-109">이 응용 프로그램과 연결 된 자격 증명을 업데이트 하려면 New-AzureRmADAppCredential cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="0f5a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0f5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="0f5a6-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f5a6-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="0f5a6-112">ObjectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7"를 사용 하 여 기존 azure active directory 응용 프로그램의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="0f5a6-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f5a6-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="0f5a6-114">ObjectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7"를 사용 하 여 기존 azure active directory 응용 프로그램의 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="0f5a6-115">변수</span><span class="sxs-lookup"><span data-stu-id="0f5a6-115">PARAMETERS</span></span>

### <span data-ttu-id="0f5a6-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0f5a6-116">-ApplicationId</span></span>
<span data-ttu-id="0f5a6-117">업데이트할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="0f5a6-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="0f5a6-119">응용 프로그램이 단일 테 넌 트 또는 다중 테 넌 트로 업데이트 되었는지 여부를 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f5a6-120">-DisplayName</span></span>
<span data-ttu-id="0f5a6-121">응용 프로그램의 새 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-122">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="0f5a6-122">-HomePage</span></span>
<span data-ttu-id="0f5a6-123">응용 프로그램 홈페이지의 새 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="0f5a6-124">-IdentifierUris</span></span>
<span data-ttu-id="0f5a6-125">응용 프로그램을 식별 하는 새 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0f5a6-126">-ObjectId</span></span>
<span data-ttu-id="0f5a6-127">업데이트할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-127">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="0f5a6-128">-ReplyUrls</span></span>
<span data-ttu-id="0f5a6-129">응용 프로그램에 대 한 새 회신 url입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5a6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0f5a6-130">-Confirm</span></span>
<span data-ttu-id="0f5a6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f5a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f5a6-132">-WhatIf</span></span>
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

### <span data-ttu-id="0f5a6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5a6-133">-DefaultProfile</span></span>
<span data-ttu-id="0f5a6-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f5a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5a6-135">CommonParameters</span></span>
<span data-ttu-id="0f5a6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5a6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f5a6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5a6-138">입력</span><span class="sxs-lookup"><span data-stu-id="0f5a6-138">INPUTS</span></span>

## <span data-ttu-id="0f5a6-139">출력</span><span class="sxs-lookup"><span data-stu-id="0f5a6-139">OUTPUTS</span></span>

### <span data-ttu-id="0f5a6-140">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="0f5a6-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0f5a6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0f5a6-141">NOTES</span></span>

## <span data-ttu-id="0f5a6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f5a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f5a6-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f5a6-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="0f5a6-144">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f5a6-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="0f5a6-145">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0f5a6-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="0f5a6-146">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f5a6-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="0f5a6-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f5a6-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="0f5a6-148">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0f5a6-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

