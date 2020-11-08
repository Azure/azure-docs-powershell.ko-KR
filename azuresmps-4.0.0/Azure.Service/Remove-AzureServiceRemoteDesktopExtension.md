---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046112"
---
# <span data-ttu-id="65aa2-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="65aa2-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="65aa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="65aa2-103">지정 된 배포 슬롯에서 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 원격 데스크톱 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="65aa2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65aa2-104">SYNTAX</span></span>

### <span data-ttu-id="65aa2-105">RemoveByRoles (기본값)</span><span class="sxs-lookup"><span data-stu-id="65aa2-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="65aa2-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="65aa2-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="65aa2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65aa2-107">DESCRIPTION</span></span>
<span data-ttu-id="65aa2-108">**Remove-AzureServiceRemoteDesktopExtension** cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 원격 데스크톱 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="65aa2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="65aa2-109">EXAMPLES</span></span>

### <span data-ttu-id="65aa2-110">예제 1: 원격 데스크톱 확장 제거</span><span class="sxs-lookup"><span data-stu-id="65aa2-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="65aa2-111">이 명령은 원격 데스크톱 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="65aa2-112">예제 2: 지정 된 역할에서 원격 데스크톱 확장 제거</span><span class="sxs-lookup"><span data-stu-id="65aa2-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="65aa2-113">이 명령은 지정 된 역할에서 원격 데스크톱 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="65aa2-114">변수</span><span class="sxs-lookup"><span data-stu-id="65aa2-114">PARAMETERS</span></span>

### <span data-ttu-id="65aa2-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="65aa2-115">-InformationAction</span></span>
<span data-ttu-id="65aa2-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="65aa2-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="65aa2-118">하기로</span><span class="sxs-lookup"><span data-stu-id="65aa2-118">Continue</span></span>
- <span data-ttu-id="65aa2-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="65aa2-119">Ignore</span></span>
- <span data-ttu-id="65aa2-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="65aa2-120">Inquire</span></span>
- <span data-ttu-id="65aa2-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="65aa2-121">SilentlyContinue</span></span>
- <span data-ttu-id="65aa2-122">중지가</span><span class="sxs-lookup"><span data-stu-id="65aa2-122">Stop</span></span>
- <span data-ttu-id="65aa2-123">대기</span><span class="sxs-lookup"><span data-stu-id="65aa2-123">Suspend</span></span>

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

### <span data-ttu-id="65aa2-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="65aa2-124">-InformationVariable</span></span>
<span data-ttu-id="65aa2-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="65aa2-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="65aa2-126">-Profile</span></span>
<span data-ttu-id="65aa2-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65aa2-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65aa2-129">-역할</span><span class="sxs-lookup"><span data-stu-id="65aa2-129">-Role</span></span>
<span data-ttu-id="65aa2-130">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="65aa2-131">지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="65aa2-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="65aa2-132">-ServiceName</span></span>
<span data-ttu-id="65aa2-133">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="65aa2-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="65aa2-134">-Slot</span></span>
<span data-ttu-id="65aa2-135">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="65aa2-136">지원 되는 값은 "생산" 또는 "준비"입니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="65aa2-137">-Installconfiguration</span><span class="sxs-lookup"><span data-stu-id="65aa2-137">-UninstallConfiguration</span></span>
<span data-ttu-id="65aa2-138">이 cmdlet이 클라우드 서비스에서 모든 RDP 구성을 제거 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="65aa2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65aa2-139">CommonParameters</span></span>
<span data-ttu-id="65aa2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65aa2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65aa2-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65aa2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65aa2-142">입력</span><span class="sxs-lookup"><span data-stu-id="65aa2-142">INPUTS</span></span>

## <span data-ttu-id="65aa2-143">출력</span><span class="sxs-lookup"><span data-stu-id="65aa2-143">OUTPUTS</span></span>

## <span data-ttu-id="65aa2-144">상속자</span><span class="sxs-lookup"><span data-stu-id="65aa2-144">NOTES</span></span>

## <span data-ttu-id="65aa2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65aa2-145">RELATED LINKS</span></span>

[<span data-ttu-id="65aa2-146">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="65aa2-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


