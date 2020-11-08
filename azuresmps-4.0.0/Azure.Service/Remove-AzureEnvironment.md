---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046477"
---
# <span data-ttu-id="896c3-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="896c3-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="896c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896c3-102">SYNOPSIS</span></span>
<span data-ttu-id="896c3-103">Windows PowerShell에서 Azure 환경을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="896c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="896c3-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="896c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="896c3-105">DESCRIPTION</span></span>
<span data-ttu-id="896c3-106">Windows PowerShell이 로밍 프로필에서 Azure 환경을 찾을 수 없도록 **제거-azureenvironment** cmdlet이 앱을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="896c3-107">이 cmdlet은 Microsoft Azure에서 환경을 삭제 하거나 모든 방법으로 실제 환경을 변경 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="896c3-108">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="896c3-109">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="896c3-110">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="896c3-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="896c3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="896c3-111">EXAMPLES</span></span>

### <span data-ttu-id="896c3-112">예제 1: 환경 삭제</span><span class="sxs-lookup"><span data-stu-id="896c3-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="896c3-113">이 명령은 Windows PowerShell에서 ContosoEnv 환경을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="896c3-114">예제 2: 여러 환경 삭제</span><span class="sxs-lookup"><span data-stu-id="896c3-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="896c3-115">이 명령은 이름이 "Contoso"로 시작 하는 환경을 Windows PowerShell에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="896c3-116">변수</span><span class="sxs-lookup"><span data-stu-id="896c3-116">PARAMETERS</span></span>

### <span data-ttu-id="896c3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="896c3-117">-Force</span></span>
<span data-ttu-id="896c3-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="896c3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="896c3-119">-Name</span></span>
<span data-ttu-id="896c3-120">제거할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="896c3-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-121">This parameter is required.</span></span>
<span data-ttu-id="896c3-122">이 매개 변수 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="896c3-123">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-123">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="896c3-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="896c3-124">-Profile</span></span>
<span data-ttu-id="896c3-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="896c3-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="896c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896c3-127">CommonParameters</span></span>
<span data-ttu-id="896c3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896c3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="896c3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896c3-130">입력</span><span class="sxs-lookup"><span data-stu-id="896c3-130">INPUTS</span></span>

### <span data-ttu-id="896c3-131">않아야</span><span class="sxs-lookup"><span data-stu-id="896c3-131">None</span></span>
<span data-ttu-id="896c3-132">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="896c3-133">출력</span><span class="sxs-lookup"><span data-stu-id="896c3-133">OUTPUTS</span></span>

### <span data-ttu-id="896c3-134">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="896c3-134">None or System.Boolean</span></span>
<span data-ttu-id="896c3-135">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="896c3-136">그렇지 않으면 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="896c3-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="896c3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="896c3-137">NOTES</span></span>

## <span data-ttu-id="896c3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="896c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="896c3-139">-AzureEnvironment 추가</span><span class="sxs-lookup"><span data-stu-id="896c3-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="896c3-140">가져오기-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="896c3-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="896c3-141">Set AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="896c3-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


