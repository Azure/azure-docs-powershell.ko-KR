---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045996"
---
# <span data-ttu-id="a8794-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a8794-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="a8794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8794-102">SYNOPSIS</span></span>
<span data-ttu-id="a8794-103">Azure RemoteApp 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a8794-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8794-104">SYNTAX</span></span>

### <span data-ttu-id="a8794-105">AllParameterSets (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8794-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a8794-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="a8794-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8794-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a8794-107">DESCRIPTION</span></span>
<span data-ttu-id="a8794-108">**AzureRemoteAppCollection** Cmdlet은 Azure RemoteApp 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a8794-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a8794-109">EXAMPLES</span></span>

### <span data-ttu-id="a8794-110">예제 1: 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="a8794-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="a8794-111">이 명령은 Azure RemoteApp 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="a8794-112">예제 2: 자격 증명을 사용 하 여 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="a8794-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="a8794-113">이 명령은 **Get-credential** cmdlet의 자격 증명을 사용 하 여 Azure RemoteApp 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="a8794-114">변수</span><span class="sxs-lookup"><span data-stu-id="a8794-114">PARAMETERS</span></span>

### <span data-ttu-id="a8794-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a8794-115">-CollectionName</span></span>
<span data-ttu-id="a8794-116">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-116">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="a8794-117">-Credential</span></span>
<span data-ttu-id="a8794-118">사용자의 도메인에 Azure RemoteApp 서버에 가입할 수 있는 권한이 있는 서비스 계정의 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="a8794-119">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="a8794-120">-CustomRdpProperty</span></span>
<span data-ttu-id="a8794-121">드라이브 리디렉션 및 기타 설정을 구성 하는 데 사용할 수 있는 사용자 지정 RDP (원격 데스크톱 Protocal) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="a8794-122">자세한 내용은 [Windows Server의 원격 데스크톱 서비스에 대 한 RDP 설정을](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) 참조 `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` 하세요.  </span><span class="sxs-lookup"><span data-stu-id="a8794-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-123">-설명</span><span class="sxs-lookup"><span data-stu-id="a8794-123">-Description</span></span>
<span data-ttu-id="a8794-124">개체에 대 한 간단한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-124">Specifies a short description for the object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="a8794-125">-DnsServers</span></span>
<span data-ttu-id="a8794-126">DNS 서버의 IPv4 주소 목록 (쉼표로 구분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-127">-도메인</span><span class="sxs-lookup"><span data-stu-id="a8794-127">-Domain</span></span>
<span data-ttu-id="a8794-128">RD 세션 호스트 서버에 참가할 Active Directory 도메인 서비스 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a8794-129">-ImageName</span></span>
<span data-ttu-id="a8794-130">Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-131">-위치</span><span class="sxs-lookup"><span data-stu-id="a8794-131">-Location</span></span>
<span data-ttu-id="a8794-132">컬렉션의 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="a8794-133">-OrganizationalUnit</span></span>
<span data-ttu-id="a8794-134">RD 세션 호스트 서버에 가입할 OU (조직 구성 단위)의 이름 (예: OU = MyOu, DC = MyDomain, DC = ParentDomain, DC = com)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="a8794-135">OU 및 DC와 같은 특성은 대/소문자를 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="a8794-136">컬렉션을 만든 후에는 OU를 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-137">-계획</span><span class="sxs-lookup"><span data-stu-id="a8794-137">-Plan</span></span>
<span data-ttu-id="a8794-138">사용 제한을 정의할 수 있는 Azure RemoteApp 컬렉션에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="a8794-139">사용할 수 있는 계획을 보려면 **get-help를 AzureRemoteAppPlan** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-140">-프로필</span><span class="sxs-lookup"><span data-stu-id="a8794-140">-Profile</span></span>
<span data-ttu-id="a8794-141">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8794-142">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8794-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a8794-143">-ResourceType</span></span>
<span data-ttu-id="a8794-144">컬렉션의 리소스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="a8794-145">이 매개 변수에 허용 되는 값은 앱 또는 데스크톱입니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a8794-146">-SubnetName</span></span>
<span data-ttu-id="a8794-147">Azure RemoteApp 컬렉션을 만드는 데 사용할 가상 네트워크 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a8794-148">-VNetName</span></span>
<span data-ttu-id="a8794-149">Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8794-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8794-150">CommonParameters</span></span>
<span data-ttu-id="a8794-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8794-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8794-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8794-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8794-153">입력</span><span class="sxs-lookup"><span data-stu-id="a8794-153">INPUTS</span></span>

## <span data-ttu-id="a8794-154">출력</span><span class="sxs-lookup"><span data-stu-id="a8794-154">OUTPUTS</span></span>

## <span data-ttu-id="a8794-155">상속자</span><span class="sxs-lookup"><span data-stu-id="a8794-155">NOTES</span></span>

## <span data-ttu-id="a8794-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8794-156">RELATED LINKS</span></span>

[<span data-ttu-id="a8794-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a8794-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="a8794-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="a8794-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="a8794-159">제거-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a8794-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="a8794-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a8794-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="a8794-161">업데이트-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a8794-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


