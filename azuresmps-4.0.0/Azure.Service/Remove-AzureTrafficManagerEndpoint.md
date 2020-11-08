---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046092"
---
# <span data-ttu-id="22f6a-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="22f6a-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="22f6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="22f6a-103">Traffic Manager 프로필에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="22f6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22f6a-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22f6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="22f6a-106">**AzureTrafficManagerEndpoint** Cmdlet은 Microsoft Azure Traffic Manager 프로필에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="22f6a-107">끝점을 제거한 후 파이프라인 연산자를 사용 하 여 결과를 **AzureTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="22f6a-108">해당 cmdlet이 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="22f6a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="22f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="22f6a-110">예제 1: 프로필에서 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="22f6a-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="22f6a-111">첫 번째 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 ContosoProfile 이라는 프로필을 가져오고이를 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="22f6a-112">두 번째 명령은 $TrafficManagerProfile에 저장 된 Traffic Manager 프로필에서 도메인 이름 Contoso02App.cloudapp.net 있는 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="22f6a-113">이 명령은 프로필 개체를 **Set-AzureTrafficManagerProfile** cmdlet에 전달 하 여 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="22f6a-114">변수</span><span class="sxs-lookup"><span data-stu-id="22f6a-114">PARAMETERS</span></span>

### <span data-ttu-id="22f6a-115">-DomainName</span><span class="sxs-lookup"><span data-stu-id="22f6a-115">-DomainName</span></span>
<span data-ttu-id="22f6a-116">제거할 끝점의 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22f6a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="22f6a-117">-Force</span></span>
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

### <span data-ttu-id="22f6a-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="22f6a-118">-Profile</span></span>
<span data-ttu-id="22f6a-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="22f6a-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22f6a-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f6a-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="22f6a-122">끝점을 제거할 Traffic Manager 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22f6a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f6a-123">CommonParameters</span></span>
<span data-ttu-id="22f6a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f6a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22f6a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f6a-126">입력</span><span class="sxs-lookup"><span data-stu-id="22f6a-126">INPUTS</span></span>

## <span data-ttu-id="22f6a-127">출력</span><span class="sxs-lookup"><span data-stu-id="22f6a-127">OUTPUTS</span></span>

### <span data-ttu-id="22f6a-128">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="22f6a-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="22f6a-129">이 cmdlet은 업데이트 된 프로필에 대 한 정보를 포함 하는 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f6a-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="22f6a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="22f6a-130">NOTES</span></span>

## <span data-ttu-id="22f6a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22f6a-131">RELATED LINKS</span></span>

[<span data-ttu-id="22f6a-132">추가-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="22f6a-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="22f6a-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="22f6a-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="22f6a-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f6a-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="22f6a-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22f6a-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


