---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046116"
---
# <span data-ttu-id="a5ae1-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a5ae1-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="a5ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ae1-103">특정 배포 슬롯에서 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="a5ae1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5ae1-104">SYNTAX</span></span>

### <span data-ttu-id="a5ae1-105">RemoveByRoles (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5ae1-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5ae1-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="a5ae1-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5ae1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5ae1-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ae1-108">**AzureServiceDiagnosticsExtension** cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="a5ae1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5ae1-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ae1-110">예제 1: 서비스에 대 한 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="a5ae1-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="a5ae1-111">이 명령은 지정 된 역할에 대 한 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="a5ae1-112">예제 2: 지정 된 역할에서 서비스에 대 한 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="a5ae1-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="a5ae1-113">이 명령은 지정 된 역할에 대 한 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="a5ae1-114">변수</span><span class="sxs-lookup"><span data-stu-id="a5ae1-114">PARAMETERS</span></span>

### <span data-ttu-id="a5ae1-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a5ae1-115">-InformationAction</span></span>
<span data-ttu-id="a5ae1-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a5ae1-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5ae1-118">하기로</span><span class="sxs-lookup"><span data-stu-id="a5ae1-118">Continue</span></span>
- <span data-ttu-id="a5ae1-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="a5ae1-119">Ignore</span></span>
- <span data-ttu-id="a5ae1-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="a5ae1-120">Inquire</span></span>
- <span data-ttu-id="a5ae1-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a5ae1-121">SilentlyContinue</span></span>
- <span data-ttu-id="a5ae1-122">중지가</span><span class="sxs-lookup"><span data-stu-id="a5ae1-122">Stop</span></span>
- <span data-ttu-id="a5ae1-123">대기</span><span class="sxs-lookup"><span data-stu-id="a5ae1-123">Suspend</span></span>

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

### <span data-ttu-id="a5ae1-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a5ae1-124">-InformationVariable</span></span>
<span data-ttu-id="a5ae1-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a5ae1-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="a5ae1-126">-Profile</span></span>
<span data-ttu-id="a5ae1-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5ae1-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5ae1-129">-역할</span><span class="sxs-lookup"><span data-stu-id="a5ae1-129">-Role</span></span>
<span data-ttu-id="a5ae1-130">원격 데스크톱 구성을 지정할 역할의 선택적 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="a5ae1-131">이 매개 변수를 지정 하지 않으면 원격 데스크톱 구성이 모든 역할에 대 한 기본 구성으로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="a5ae1-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5ae1-132">-ServiceName</span></span>
<span data-ttu-id="a5ae1-133">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="a5ae1-134">-슬롯</span><span class="sxs-lookup"><span data-stu-id="a5ae1-134">-Slot</span></span>
<span data-ttu-id="a5ae1-135">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="a5ae1-136">유효한 값은 제작 또는 준비입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="a5ae1-137">-Installconfiguration</span><span class="sxs-lookup"><span data-stu-id="a5ae1-137">-UninstallConfiguration</span></span>
<span data-ttu-id="a5ae1-138">이 cmdlet이 클라우드 서비스에서 모든 RDP 구성을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="a5ae1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ae1-139">CommonParameters</span></span>
<span data-ttu-id="a5ae1-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ae1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ae1-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ae1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ae1-142">입력</span><span class="sxs-lookup"><span data-stu-id="a5ae1-142">INPUTS</span></span>

## <span data-ttu-id="a5ae1-143">출력</span><span class="sxs-lookup"><span data-stu-id="a5ae1-143">OUTPUTS</span></span>

## <span data-ttu-id="a5ae1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="a5ae1-144">NOTES</span></span>

## <span data-ttu-id="a5ae1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5ae1-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5ae1-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a5ae1-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="a5ae1-147">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a5ae1-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


