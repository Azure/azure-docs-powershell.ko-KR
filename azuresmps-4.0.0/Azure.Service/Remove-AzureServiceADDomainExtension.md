---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046126"
---
# <span data-ttu-id="4bfc5-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4bfc5-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="4bfc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfc5-103">특정 배포 슬롯에서 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 AD 도메인 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="4bfc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bfc5-104">SYNTAX</span></span>

### <span data-ttu-id="4bfc5-105">RemoveByRoles (기본값)</span><span class="sxs-lookup"><span data-stu-id="4bfc5-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bfc5-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="4bfc5-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bfc5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4bfc5-107">DESCRIPTION</span></span>
<span data-ttu-id="4bfc5-108">**Remove-AzureServiceADDomainExtension** cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 된 AD (클라우드 서비스 Active Directory) 도메인 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="4bfc5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4bfc5-109">EXAMPLES</span></span>

### <span data-ttu-id="4bfc5-110">예제 1: AD 도메인 확장 제거</span><span class="sxs-lookup"><span data-stu-id="4bfc5-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="4bfc5-111">이 명령은 $Svc 변수로 지정 된 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="4bfc5-112">예제 2: 지정 된 역할에 대 한 AD 도메인 확장 제거</span><span class="sxs-lookup"><span data-stu-id="4bfc5-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="4bfc5-113">이 명령은 지정 된 역할에 대 한 서비스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="4bfc5-114">변수</span><span class="sxs-lookup"><span data-stu-id="4bfc5-114">PARAMETERS</span></span>

### <span data-ttu-id="4bfc5-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4bfc5-115">-InformationAction</span></span>
<span data-ttu-id="4bfc5-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4bfc5-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4bfc5-118">하기로</span><span class="sxs-lookup"><span data-stu-id="4bfc5-118">Continue</span></span>
- <span data-ttu-id="4bfc5-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="4bfc5-119">Ignore</span></span>
- <span data-ttu-id="4bfc5-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="4bfc5-120">Inquire</span></span>
- <span data-ttu-id="4bfc5-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4bfc5-121">SilentlyContinue</span></span>
- <span data-ttu-id="4bfc5-122">중지가</span><span class="sxs-lookup"><span data-stu-id="4bfc5-122">Stop</span></span>
- <span data-ttu-id="4bfc5-123">대기</span><span class="sxs-lookup"><span data-stu-id="4bfc5-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4bfc5-124">-InformationVariable</span></span>
<span data-ttu-id="4bfc5-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="4bfc5-126">-Profile</span></span>
<span data-ttu-id="4bfc5-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bfc5-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bfc5-129">-역할</span><span class="sxs-lookup"><span data-stu-id="4bfc5-129">-Role</span></span>
<span data-ttu-id="4bfc5-130">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="4bfc5-131">지정 하지 않으면 AD 도메인 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4bfc5-132">-ServiceName</span></span>
<span data-ttu-id="4bfc5-133">Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-133">Specifies the name of an Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4bfc5-134">-Slot</span></span>
<span data-ttu-id="4bfc5-135">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4bfc5-136">유효한 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-136">Valid values are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-137">-Installconfiguration</span><span class="sxs-lookup"><span data-stu-id="4bfc5-137">-UninstallConfiguration</span></span>
<span data-ttu-id="4bfc5-138">이 cmdlet이 클라우드 서비스에서 모든 AD 도메인 구성을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bfc5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfc5-139">CommonParameters</span></span>
<span data-ttu-id="4bfc5-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bfc5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfc5-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bfc5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfc5-142">입력</span><span class="sxs-lookup"><span data-stu-id="4bfc5-142">INPUTS</span></span>

## <span data-ttu-id="4bfc5-143">출력</span><span class="sxs-lookup"><span data-stu-id="4bfc5-143">OUTPUTS</span></span>

## <span data-ttu-id="4bfc5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4bfc5-144">NOTES</span></span>

## <span data-ttu-id="4bfc5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bfc5-145">RELATED LINKS</span></span>

[<span data-ttu-id="4bfc5-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4bfc5-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="4bfc5-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="4bfc5-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


